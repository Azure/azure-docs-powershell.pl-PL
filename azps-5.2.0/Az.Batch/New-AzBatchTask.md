---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 043e7bf24ce994edd0ce5621d2de8b17616d43f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361291"
---
# <span data-ttu-id="4f877-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4f877-101">New-AzBatchTask</span></span>

## <span data-ttu-id="4f877-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f877-102">SYNOPSIS</span></span>
<span data-ttu-id="4f877-103">Umożliwia utworzenie zadania wsadowego w ramach zadania.</span><span class="sxs-lookup"><span data-stu-id="4f877-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="4f877-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f877-104">SYNTAX</span></span>

### <span data-ttu-id="4f877-105">JobId_Single (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="4f877-105">JobId_Single (Default)</span></span>
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f877-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="4f877-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f877-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="4f877-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f877-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="4f877-108">JobObject_Single</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f877-109">Opis</span><span class="sxs-lookup"><span data-stu-id="4f877-109">DESCRIPTION</span></span>
<span data-ttu-id="4f877-110">Polecenie cmdlet **New-AzBatchTask** tworzy zadanie wsadowe platformy Azure w ramach zadania określonego przez parametr *JobID* lub parametr *zadania* .</span><span class="sxs-lookup"><span data-stu-id="4f877-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="4f877-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f877-111">EXAMPLES</span></span>

### <span data-ttu-id="4f877-112">Przykład 1. Tworzenie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="4f877-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="4f877-113">To polecenie tworzy zadanie o IDENTYFIKATORze Task23 w ramach zadania o identyfikatorze Job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="4f877-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="4f877-114">Zadanie uruchamia określone polecenie.</span><span class="sxs-lookup"><span data-stu-id="4f877-114">The task runs the specified command.</span></span>
<span data-ttu-id="4f877-115">Użyj polecenia cmdlet **Get-AzBatchAccountKey** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="4f877-115">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="4f877-116">Przykład 2: Tworzenie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="4f877-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="4f877-117">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze zadania w 000001, używając polecenia cmdlet **Get-AzBatchJob** .</span><span class="sxs-lookup"><span data-stu-id="4f877-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="4f877-118">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="4f877-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4f877-119">Polecenie utworzy zadanie o IDENTYFIKATORze Task26 w ramach tego zadania.</span><span class="sxs-lookup"><span data-stu-id="4f877-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="4f877-120">Zadanie uruchamia określone polecenie, korzystając z podniesionych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="4f877-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="4f877-121">Przykład 3: Dodawanie kolekcji zadań do określonego zadania za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="4f877-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="4f877-122">Pierwsze polecenie tworzy odwołanie obiektu do kluczy konta dla konta wsadowego o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="4f877-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="4f877-123">Polecenie zapisuje to odwołanie do obiektu w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="4f877-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="4f877-124">Następne dwa polecenia tworzą **PSCloudTask** obiekty za pomocą polecenia cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="4f877-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="4f877-125">Te polecenia przechowują zadania w zmiennych $Task 01 i $Task 02.</span><span class="sxs-lookup"><span data-stu-id="4f877-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="4f877-126">Polecenie ostatnie pobiera zadanie wsadowe o IDENTYFIKATORze Job-000001 przy użyciu polecenia **Get-AzBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="4f877-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="4f877-127">Następnie polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="4f877-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4f877-128">Polecenie dodaje kolekcję zadań w ramach tego zadania.</span><span class="sxs-lookup"><span data-stu-id="4f877-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="4f877-129">Polecenie używa kontekstu przechowywanego w $Context.</span><span class="sxs-lookup"><span data-stu-id="4f877-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="4f877-130">Przykład 4: Dodawanie zestawu zadań do określonego zadania</span><span class="sxs-lookup"><span data-stu-id="4f877-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="4f877-131">Pierwsze polecenie tworzy odwołanie obiektu do kluczy konta dla konta wsadowego o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="4f877-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="4f877-132">Polecenie zapisuje to odwołanie do obiektu w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="4f877-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="4f877-133">Następne dwa polecenia tworzą **PSCloudTask** obiekty za pomocą polecenia cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="4f877-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="4f877-134">Te polecenia przechowują zadania w zmiennych $Task 01 i $Task 02.</span><span class="sxs-lookup"><span data-stu-id="4f877-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="4f877-135">Polecenie ostatnie umożliwia dodanie zadań przechowywanych w $Task 01 i $Task 02 w ramach zadania o identyfikatorze ID-000001.</span><span class="sxs-lookup"><span data-stu-id="4f877-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="4f877-136">Przykład 5: Dodawanie zadania z plikami wyjściowymi</span><span class="sxs-lookup"><span data-stu-id="4f877-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="4f877-137">Przykład 6: Dodawanie zadania z ustawieniami tokenu uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="4f877-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="4f877-138">Przykład 7: Dodawanie zadania działającego w kontenerze</span><span class="sxs-lookup"><span data-stu-id="4f877-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="4f877-139">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f877-139">PARAMETERS</span></span>

### <span data-ttu-id="4f877-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="4f877-140">-AffinityInformation</span></span>
<span data-ttu-id="4f877-141">Określa wskazówkę o lokalizacji, której usługa wsadowa używa do zaznaczania węzła, na którym ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="4f877-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="4f877-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="4f877-142">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f877-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="4f877-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="4f877-144">Ustawienia tokenu uwierzytelniania, za pomocą którego zadanie może wykonywać operacje usługi wsadowej.</span><span class="sxs-lookup"><span data-stu-id="4f877-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="4f877-145">Jeśli to ustawienie jest skonfigurowane, usługa przetwarzania wsadowego dostarcza zadanie z tokenem uwierzytelniania, którego można użyć do uwierzytelniania operacji usługi przetwarzania wsadowego bez konieczności korzystania z klucza dostępu do konta.</span><span class="sxs-lookup"><span data-stu-id="4f877-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="4f877-146">Token jest dostarczany za pośrednictwem zmiennej środowiskowej AZ_BATCH_AUTHENTICATION_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="4f877-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="4f877-147">Operacje, które mogą być wykonywane przez zadanie przy użyciu tokenu, zależą od ustawień.</span><span class="sxs-lookup"><span data-stu-id="4f877-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="4f877-148">Na przykład zadanie może zażądać uprawnień do zadania, aby można było dodać do zadania inne zadania lub sprawdzić stan zadania lub innych zadań.</span><span class="sxs-lookup"><span data-stu-id="4f877-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f877-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4f877-149">-BatchContext</span></span>
<span data-ttu-id="4f877-150">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="4f877-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4f877-151">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="4f877-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4f877-152">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="4f877-152">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4f877-153">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="4f877-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4f877-154">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4f877-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4f877-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="4f877-155">-CommandLine</span></span>
<span data-ttu-id="4f877-156">Określa wiersz polecenia dla zadania.</span><span class="sxs-lookup"><span data-stu-id="4f877-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="4f877-157">-Ograniczenia</span><span class="sxs-lookup"><span data-stu-id="4f877-157">-Constraints</span></span>
<span data-ttu-id="4f877-158">Określa ograniczenia wykonania dotyczące tego zadania.</span><span class="sxs-lookup"><span data-stu-id="4f877-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="4f877-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="4f877-159">-ContainerSettings</span></span>
<span data-ttu-id="4f877-160">Ustawienia kontenera, w którym jest uruchamiane zadanie.</span><span class="sxs-lookup"><span data-stu-id="4f877-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="4f877-161">Jeśli Pula, która będzie uruchamiać to zadanie, ma ustawiony containerConfiguration, należy ją również ustawić.</span><span class="sxs-lookup"><span data-stu-id="4f877-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="4f877-162">Jeśli Pula, która będzie uruchamiać to zadanie, nie ma ustawionego zestawu containerConfiguration, nie może być ustawiona.</span><span class="sxs-lookup"><span data-stu-id="4f877-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="4f877-163">Jeśli ta funkcja jest określona, wszystkie katalogi rekursywnie poniżej AZ_BATCH_NODE_ROOT_DIR (katalog główny katalogów usługi Azure Batch w węźle) są mapowane na kontener, wszystkie zmienne środowiskowe zadań są mapowane na kontener, a wiersz polecenia zadanie jest wykonywany w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="4f877-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f877-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f877-164">-DefaultProfile</span></span>
<span data-ttu-id="4f877-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f877-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f877-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="4f877-166">-DependsOn</span></span>
<span data-ttu-id="4f877-167">Określa, że zadanie zależy od innych zadań.</span><span class="sxs-lookup"><span data-stu-id="4f877-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="4f877-168">Zadanie nie zostanie zaplanowane, dopóki wszystkie zadania zależne od siebie nie zostaną pomyślnie ukończone.</span><span class="sxs-lookup"><span data-stu-id="4f877-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="4f877-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4f877-169">-DisplayName</span></span>
<span data-ttu-id="4f877-170">Określa nazwę wyświetlaną zadania.</span><span class="sxs-lookup"><span data-stu-id="4f877-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="4f877-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="4f877-171">-EnvironmentSettings</span></span>
<span data-ttu-id="4f877-172">Określa ustawienia środowiska jako pary klucz/wartość, które to polecenie cmdlet dodaje do zadania.</span><span class="sxs-lookup"><span data-stu-id="4f877-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="4f877-173">Klucz jest nazwą ustawienia środowiska.</span><span class="sxs-lookup"><span data-stu-id="4f877-173">The key is the environment setting name.</span></span>
<span data-ttu-id="4f877-174">Wartość to ustawienie środowiska.</span><span class="sxs-lookup"><span data-stu-id="4f877-174">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f877-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="4f877-175">-ExitConditions</span></span>
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

### <span data-ttu-id="4f877-176">-ID</span><span class="sxs-lookup"><span data-stu-id="4f877-176">-Id</span></span>
<span data-ttu-id="4f877-177">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="4f877-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="4f877-178">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="4f877-178">-Job</span></span>
<span data-ttu-id="4f877-179">Określa zadanie, za pomocą którego to polecenie cmdlet tworzy zadanie.</span><span class="sxs-lookup"><span data-stu-id="4f877-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="4f877-180">Aby uzyskać obiekt **PSCloudJob** , użyj polecenia cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="4f877-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="4f877-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="4f877-181">-JobId</span></span>
<span data-ttu-id="4f877-182">Określa identyfikator zadania, za pomocą którego to polecenie cmdlet tworzy zadanie.</span><span class="sxs-lookup"><span data-stu-id="4f877-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="4f877-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="4f877-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="4f877-184">Określa informacje dotyczące uruchamiania zadania o wielu wystąpieniach.</span><span class="sxs-lookup"><span data-stu-id="4f877-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="4f877-185">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="4f877-185">-OutputFile</span></span>
<span data-ttu-id="4f877-186">Pobiera lub ustawia listę plików, które usługa wsadowa przekaże z węzła obliczeniowego po uruchomieniu wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="4f877-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="4f877-187">W przypadku zadań o wielu wystąpieniach pliki będą przekazywane tylko z węzła obliczeniowego, na którym jest wykonywane zadanie główne.</span><span class="sxs-lookup"><span data-stu-id="4f877-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f877-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="4f877-188">-ResourceFiles</span></span>
<span data-ttu-id="4f877-189">Określa pliki zasobów, takie jak pary klucz/wartość, których wymaga zadanie.</span><span class="sxs-lookup"><span data-stu-id="4f877-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="4f877-190">Klucz to ścieżka pliku zasobu.</span><span class="sxs-lookup"><span data-stu-id="4f877-190">The key is the resource file path.</span></span>
<span data-ttu-id="4f877-191">Wartość to źródło obiektów blob pliku zasobów.</span><span class="sxs-lookup"><span data-stu-id="4f877-191">The value is the resource file blob source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSResourceFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f877-192">-Zadania</span><span class="sxs-lookup"><span data-stu-id="4f877-192">-Tasks</span></span>
<span data-ttu-id="4f877-193">Określa kolekcję zadań, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="4f877-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="4f877-194">Każde zadanie musi mieć unikatowy identyfikator.</span><span class="sxs-lookup"><span data-stu-id="4f877-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="4f877-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="4f877-195">-UserIdentity</span></span>
<span data-ttu-id="4f877-196">Tożsamość użytkownika, pod którą jest uruchamiane zadanie.</span><span class="sxs-lookup"><span data-stu-id="4f877-196">The user identity under which the task runs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f877-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f877-197">CommonParameters</span></span>
<span data-ttu-id="4f877-198">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f877-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f877-199">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f877-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f877-200">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f877-200">INPUTS</span></span>

### <span data-ttu-id="4f877-201">Microsoft.Azure.Commands.Batch. Modele. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="4f877-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="4f877-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4f877-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4f877-203">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f877-203">OUTPUTS</span></span>

### <span data-ttu-id="4f877-204">System. void</span><span class="sxs-lookup"><span data-stu-id="4f877-204">System.Void</span></span>

## <span data-ttu-id="4f877-205">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f877-205">NOTES</span></span>

## <span data-ttu-id="4f877-206">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f877-206">RELATED LINKS</span></span>

[<span data-ttu-id="4f877-207">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4f877-207">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4f877-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4f877-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="4f877-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4f877-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="4f877-210">Nowe — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4f877-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="4f877-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4f877-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="4f877-212">Zatrzymaj — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4f877-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="4f877-213">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="4f877-213">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
