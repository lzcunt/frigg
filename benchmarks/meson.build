benchmark_dep = dependency('benchmark_main', required: true, native: true)
mimalloc_dep = dependency('mimalloc', required: true, native: true)

benchmark_executable = executable('frigg_benchmarks',
	'allocators.cpp',
	'support.cpp',
	dependencies: [
		frigg_dep,
		benchmark_dep,
		mimalloc_dep,
	],
	override_options: ['cpp_std=c++23'],
	native: true,
	install: false
)

benchmark(
	'frigg benchmarks',
	benchmark_executable,
)
