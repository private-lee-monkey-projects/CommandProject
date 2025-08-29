# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a personal workflow management repository for **Flux AI model training** focused on generating Chinese traditional clothing imagery. The repository tracks training schedules, command templates, and progress logs for various model fine-tuning tasks.

## Project Structure

- `daily train.md` - Chinese daily training schedule and progress tracking
- `python.sh` - Shell script containing training command templates
- `.claude/settings.local.json` - Claude Code configuration with git permissions

## Key Training Commands

All training commands are stored in `python.sh` and use Kohya SS training scripts:

### LoRA Training
- Single image LoRA: Uses `--single_image` flag with specific style prompts
- Full dataset LoRA: Standard LoRA training with multiple images

### DreamBooth Training  
- Single image DreamBooth: Uses `--single_image` flag
- Full dataset DreamBooth: Standard DreamBooth training

### Common Parameters
- Model: Flux-based models for different clothing styles (汉女, 汉男, 唐男, 明女, 明男)
- Platform: Remote GPU training via console.d.run
- Hardware: H800 GPU instances

## Workflow Management

Training progress is tracked manually in `daily train.md` which includes:
- Daily schedules by clothing category
- GPU usage tracking
- Training completion status
- Next steps planning

## Development Notes

- No traditional build/test/lint commands - this is a script collection repository
- Documentation is primarily in Chinese
- Commands require remote GPU access and Hugging Face authentication
- Training sessions are manually scheduled and monitored

## Git Configuration

- Main branch: `master`
- Remote: `https://github.com/private-lee-monkey-projects/CommandProject.git`
- Claude has limited git permissions (log operations only)