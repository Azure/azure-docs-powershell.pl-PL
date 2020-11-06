---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547052"
---
# <span data-ttu-id="65d6b-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="65d6b-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="65d6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="65d6b-103">Umożliwia utworzenie zadania wsadowego w ramach zadania.</span><span class="sxs-lookup"><span data-stu-id="65d6b-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65d6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65d6b-104">SYNTAX</span></span>

### <span data-ttu-id="65d6b-105">JobId_Single (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="65d6b-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65d6b-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="65d6b-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65d6b-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="65d6b-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65d6b-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="65d6b-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65d6b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="65d6b-109">DESCRIPTION</span></span>
<span data-ttu-id="65d6b-110">Polecenie cmdlet **New-AzureBatchTask** tworzy zadanie wsadowe platformy Azure w ramach zadania określonego przez parametr *JobID* lub parametr *zadania* .</span><span class="sxs-lookup"><span data-stu-id="65d6b-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="65d6b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65d6b-111">EXAMPLES</span></span>

### <span data-ttu-id="65d6b-112">Przykład 1. Tworzenie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="65d6b-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="65d6b-113">To polecenie tworzy zadanie o IDENTYFIKATORze Task23 w ramach zadania o identyfikatorze Job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="65d6b-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="65d6b-114">Zadanie uruchamia określone polecenie.</span><span class="sxs-lookup"><span data-stu-id="65d6b-114">The task runs the specified command.</span></span>
<span data-ttu-id="65d6b-115">Użyj polecenia cmdlet **Get-AzureRmBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="65d6b-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="65d6b-116">Przykład 2: Tworzenie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="65d6b-116">Example 2: Create a Batch task</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

<span data-ttu-id="65d6b-117">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze zadania w 000001, używając polecenia cmdlet **Get-AzureBatchJob** .</span><span class="sxs-lookup"><span data-stu-id="65d6b-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="65d6b-118">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="65d6b-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="65d6b-119">Polecenie utworzy zadanie o IDENTYFIKATORze Task26 w ramach tego zadania.</span><span class="sxs-lookup"><span data-stu-id="65d6b-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="65d6b-120">Zadanie uruchamia określone polecenie, korzystając z podniesionych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="65d6b-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="65d6b-121">Przykład 3: Dodawanie kolekcji zadań do określonego zadania za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="65d6b-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="65d6b-122">Pierwsze polecenie tworzy odwołanie obiektu do kluczy konta dla konta wsadowego o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="65d6b-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="65d6b-123">Polecenie zapisuje to odwołanie do obiektu w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="65d6b-123">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="65d6b-124">Następne dwa polecenia tworzą **PSCloudTask** obiekty za pomocą polecenia cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="65d6b-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="65d6b-125">Te polecenia przechowują zadania w zmiennych $Task 01 i $Task 02.</span><span class="sxs-lookup"><span data-stu-id="65d6b-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="65d6b-126">Polecenie ostatnie pobiera zadanie wsadowe o IDENTYFIKATORze Job-000001 przy użyciu polecenia **Get-AzureBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="65d6b-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="65d6b-127">Następnie polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="65d6b-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="65d6b-128">Polecenie dodaje kolekcję zadań w ramach tego zadania.</span><span class="sxs-lookup"><span data-stu-id="65d6b-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="65d6b-129">Polecenie używa kontekstu przechowywanego w $Context.</span><span class="sxs-lookup"><span data-stu-id="65d6b-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="65d6b-130">Przykład 4: Dodawanie zestawu zadań do określonego zadania</span><span class="sxs-lookup"><span data-stu-id="65d6b-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="65d6b-131">Pierwsze polecenie tworzy odwołanie obiektu do kluczy konta dla konta wsadowego o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="65d6b-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="65d6b-132">Polecenie zapisuje to odwołanie do obiektu w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="65d6b-132">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="65d6b-133">Następne dwa polecenia tworzą **PSCloudTask** obiekty za pomocą polecenia cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="65d6b-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="65d6b-134">Te polecenia przechowują zadania w zmiennych $Task 01 i $Task 02.</span><span class="sxs-lookup"><span data-stu-id="65d6b-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="65d6b-135">Polecenie ostatnie umożliwia dodanie zadań przechowywanych w $Task 01 i $Task 02 w ramach zadania o identyfikatorze ID-000001.</span><span class="sxs-lookup"><span data-stu-id="65d6b-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

## <span data-ttu-id="65d6b-136">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65d6b-136">PARAMETERS</span></span>

### <span data-ttu-id="65d6b-137">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="65d6b-137">-AffinityInformation</span></span>
<span data-ttu-id="65d6b-138">Określa wskazówkę o lokalizacji, której usługa wsadowa używa do zaznaczania węzła, na którym ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="65d6b-138">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-139">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="65d6b-139">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="65d6b-140">-BatchContext</span></span>
<span data-ttu-id="65d6b-141">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="65d6b-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="65d6b-142">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="65d6b-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-143">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="65d6b-143">-CommandLine</span></span>
<span data-ttu-id="65d6b-144">Określa wiersz polecenia dla zadania.</span><span class="sxs-lookup"><span data-stu-id="65d6b-144">Specifies the command line for the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-145">-Ograniczenia</span><span class="sxs-lookup"><span data-stu-id="65d6b-145">-Constraints</span></span>
<span data-ttu-id="65d6b-146">Określa ograniczenia wykonania dotyczące tego zadania.</span><span class="sxs-lookup"><span data-stu-id="65d6b-146">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-147">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="65d6b-147">-DependsOn</span></span>
<span data-ttu-id="65d6b-148">Określa, że zadanie zależy od innych zadań.</span><span class="sxs-lookup"><span data-stu-id="65d6b-148">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="65d6b-149">Zadanie nie zostanie zaplanowane, dopóki wszystkie zadania zależne od siebie nie zostaną pomyślnie ukończone.</span><span class="sxs-lookup"><span data-stu-id="65d6b-149">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-150">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="65d6b-150">-DisplayName</span></span>
<span data-ttu-id="65d6b-151">Określa nazwę wyświetlaną zadania.</span><span class="sxs-lookup"><span data-stu-id="65d6b-151">Specifies the display name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-152">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="65d6b-152">-EnvironmentSettings</span></span>
<span data-ttu-id="65d6b-153">Określa ustawienia środowiska jako pary klucz/wartość, które to polecenie cmdlet dodaje do zadania.</span><span class="sxs-lookup"><span data-stu-id="65d6b-153">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="65d6b-154">Klucz jest nazwą ustawienia środowiska.</span><span class="sxs-lookup"><span data-stu-id="65d6b-154">The key is the environment setting name.</span></span>
<span data-ttu-id="65d6b-155">Wartość to ustawienie środowiska.</span><span class="sxs-lookup"><span data-stu-id="65d6b-155">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-156">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="65d6b-156">-ExitConditions</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-157">-ID</span><span class="sxs-lookup"><span data-stu-id="65d6b-157">-Id</span></span>
<span data-ttu-id="65d6b-158">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="65d6b-158">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-159">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="65d6b-159">-Job</span></span>
<span data-ttu-id="65d6b-160">Określa zadanie, za pomocą którego to polecenie cmdlet tworzy zadanie.</span><span class="sxs-lookup"><span data-stu-id="65d6b-160">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="65d6b-161">Aby uzyskać obiekt **PSCloudJob** , użyj polecenia cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="65d6b-161">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="65d6b-162">-JobId</span></span>
<span data-ttu-id="65d6b-163">Określa identyfikator zadania, za pomocą którego to polecenie cmdlet tworzy zadanie.</span><span class="sxs-lookup"><span data-stu-id="65d6b-163">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-164">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="65d6b-164">-MultiInstanceSettings</span></span>
<span data-ttu-id="65d6b-165">Określa informacje dotyczące uruchamiania zadania o wielu wystąpieniach.</span><span class="sxs-lookup"><span data-stu-id="65d6b-165">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-166">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="65d6b-166">-ResourceFiles</span></span>
<span data-ttu-id="65d6b-167">Określa pliki zasobów, takie jak pary klucz/wartość, których wymaga zadanie.</span><span class="sxs-lookup"><span data-stu-id="65d6b-167">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="65d6b-168">Klucz to ścieżka pliku zasobu.</span><span class="sxs-lookup"><span data-stu-id="65d6b-168">The key is the resource file path.</span></span>
<span data-ttu-id="65d6b-169">Wartość to źródło obiektów blob pliku zasobów.</span><span class="sxs-lookup"><span data-stu-id="65d6b-169">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-170">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="65d6b-170">-RunElevated</span></span>
<span data-ttu-id="65d6b-171">Wskazuje, że proces zadania jest uruchamiany z uprawnieniami administratora.</span><span class="sxs-lookup"><span data-stu-id="65d6b-171">Indicates that the task process runs with administrator privileges.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-172">-Zadania</span><span class="sxs-lookup"><span data-stu-id="65d6b-172">-Tasks</span></span>
<span data-ttu-id="65d6b-173">Określa kolekcję zadań, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="65d6b-173">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="65d6b-174">Każde zadanie musi mieć unikatowy identyfikator.</span><span class="sxs-lookup"><span data-stu-id="65d6b-174">Each task must have a unique ID.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d6b-175">-DefaultProfile</span></span>
<span data-ttu-id="65d6b-176">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65d6b-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d6b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d6b-177">CommonParameters</span></span>
<span data-ttu-id="65d6b-178">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65d6b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d6b-179">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d6b-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d6b-180">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65d6b-180">INPUTS</span></span>

### <span data-ttu-id="65d6b-181">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="65d6b-181">BatchAccountContext</span></span>
<span data-ttu-id="65d6b-182">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="65d6b-182">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="65d6b-183">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="65d6b-183">PSCloudJob</span></span>
<span data-ttu-id="65d6b-184">Parametr "zadanie" akceptuje wartość typu "PSCloudJob" z potoku.</span><span class="sxs-lookup"><span data-stu-id="65d6b-184">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="65d6b-185">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65d6b-185">OUTPUTS</span></span>

## <span data-ttu-id="65d6b-186">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65d6b-186">NOTES</span></span>

## <span data-ttu-id="65d6b-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65d6b-187">RELATED LINKS</span></span>

[<span data-ttu-id="65d6b-188">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="65d6b-188">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="65d6b-189">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="65d6b-189">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="65d6b-190">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="65d6b-190">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="65d6b-191">Nowe — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="65d6b-191">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="65d6b-192">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="65d6b-192">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="65d6b-193">Zatrzymaj — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="65d6b-193">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="65d6b-194">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="65d6b-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


