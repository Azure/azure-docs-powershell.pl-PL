---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 254c9290b2cc838dc7ec53c2590d8505c24c1b69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992958"
---
# <span data-ttu-id="7ac0a-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7ac0a-101">New-AzBatchTask</span></span>

## <span data-ttu-id="7ac0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ac0a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac0a-103">Tworzy zadanie wsadowe w obszarze zadania.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="7ac0a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7ac0a-104">SYNTAX</span></span>

### <span data-ttu-id="7ac0a-105">JobId_Single (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7ac0a-105">JobId_Single (Default)</span></span>
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

### <span data-ttu-id="7ac0a-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="7ac0a-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ac0a-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="7ac0a-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ac0a-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="7ac0a-108">JobObject_Single</span></span>
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

## <span data-ttu-id="7ac0a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="7ac0a-109">DESCRIPTION</span></span>
<span data-ttu-id="7ac0a-110">Polecenie **cmdlet New-AzBatchTask** tworzy zadanie usługi Azure Batch w ramach zadania określonego przez parametr *JobId* lub *parametr Job.*</span><span class="sxs-lookup"><span data-stu-id="7ac0a-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="7ac0a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7ac0a-111">EXAMPLES</span></span>

### <span data-ttu-id="7ac0a-112">Przykład 1. Tworzenie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="7ac0a-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="7ac0a-113">To polecenie tworzy zadanie o identyfikatorze Zadanie23 w ramach zadania o identyfikatorze Zadanie 000001.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="7ac0a-114">Zadanie zostanie uruchamiane zgodnie z określonym poleceniem.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-114">The task runs the specified command.</span></span>
<span data-ttu-id="7ac0a-115">Użyj polecenia **cmdlet Get-AzBatchAccountKey,** aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-115">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7ac0a-116">Przykład 2. Tworzenie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="7ac0a-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="7ac0a-117">To polecenie pobiera zadanie Batch o identyfikatorze Zadanie-000001 przy użyciu polecenia cmdlet **Get-AzBatchJob.**</span><span class="sxs-lookup"><span data-stu-id="7ac0a-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="7ac0a-118">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7ac0a-119">To polecenie tworzy zadanie o identyfikatorze Zadanie26 w ramach tego zadania.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="7ac0a-120">Zadanie jest uruchamiane za pomocą określonego polecenia z podwyższonym poziomem uprawnień.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="7ac0a-121">Przykład 3. Dodawanie zbioru zadań do określonego zadania przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="7ac0a-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="7ac0a-122">Pierwsze polecenie tworzy odwołanie do obiektu do kluczy konta dla konta partii o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="7ac0a-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="7ac0a-123">Polecenie przechowuje to odwołanie do obiektu w $Context zmienną.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="7ac0a-124">Następne dwa polecenia tworzą **obiekty PSCloudTask** przy użyciu New-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="7ac0a-125">Polecenia przechowują zadania w $Task 01 i $Task 02.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="7ac0a-126">Końcowe polecenie otrzymuje zadanie Batch o identyfikatorze Zadanie-000001 przy użyciu polecenia **Get-AzBatchJob.**</span><span class="sxs-lookup"><span data-stu-id="7ac0a-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="7ac0a-127">Następnie polecenie przekazuje to zadanie do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7ac0a-128">To polecenie powoduje dodanie kolekcji zadań w ramach tego zadania.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="7ac0a-129">To polecenie używa kontekstu przechowywanego w $Context.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="7ac0a-130">Przykład 4. Dodawanie kolekcji zadań do określonego zadania</span><span class="sxs-lookup"><span data-stu-id="7ac0a-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="7ac0a-131">Pierwsze polecenie tworzy odwołanie do obiektu do kluczy konta dla konta partii o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="7ac0a-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="7ac0a-132">Polecenie przechowuje to odwołanie do obiektu w $Context zmienną.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="7ac0a-133">Następne dwa polecenia tworzą **obiekty PSCloudTask** przy użyciu New-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="7ac0a-134">Polecenia przechowują zadania w $Task 01 i $Task 02.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="7ac0a-135">Ostatnie polecenie powoduje dodanie zadań przechowywanych w $Task 01 i $Task 02 pod zadaniem o identyfikatorze Zadanie 000001.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="7ac0a-136">Przykład 5. Dodawanie zadania z plikami wyjściowmi</span><span class="sxs-lookup"><span data-stu-id="7ac0a-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="7ac0a-137">Przykład 6. Dodawanie zadania z ustawieniami tokenu uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="7ac0a-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="7ac0a-138">Przykład 7. Dodawanie zadania uruchamianego w kontenerze</span><span class="sxs-lookup"><span data-stu-id="7ac0a-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="7ac0a-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ac0a-139">PARAMETERS</span></span>

### <span data-ttu-id="7ac0a-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="7ac0a-140">-AffinityInformation</span></span>
<span data-ttu-id="7ac0a-141">Określa wskazówkę lokalizacji używaną przez usługę Batch do wybierania węzła, w którym ma być uruchamiane zadanie.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="7ac0a-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="7ac0a-142">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="7ac0a-143">—AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="7ac0a-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="7ac0a-144">Ustawienia tokenu uwierzytelniania, za pomocą których zadanie może wykonywać operacje usługi wsadowej.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="7ac0a-145">Jeśli ta wartość jest ustawiona, usługa wsadowa udostępnia zadanie z tokenem uwierzytelniania, który może być używany do uwierzytelniania operacji usługi wsadowej bez konieczności użycia klucza dostępu do konta.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="7ac0a-146">Token jest dostarczany za pośrednictwem AZ_BATCH_AUTHENTICATION_TOKEN środowiskowej.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="7ac0a-147">Operacje, które zadanie może wykonać przy użyciu tokenu, zależą od ustawień.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="7ac0a-148">Na przykład zadanie może zażądać uprawnień zadań w celu dodania innych zadań do zadania lub sprawdzić stan zadania lub innych zadań.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

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

### <span data-ttu-id="7ac0a-149">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="7ac0a-149">-BatchContext</span></span>
<span data-ttu-id="7ac0a-150">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7ac0a-151">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7ac0a-152">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-152">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7ac0a-153">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7ac0a-154">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7ac0a-155">—CommandLine</span><span class="sxs-lookup"><span data-stu-id="7ac0a-155">-CommandLine</span></span>
<span data-ttu-id="7ac0a-156">Określa wiersz polecenia zadania.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="7ac0a-157">— Ograniczenia</span><span class="sxs-lookup"><span data-stu-id="7ac0a-157">-Constraints</span></span>
<span data-ttu-id="7ac0a-158">Określa ograniczenia wykonywania, które mają zastosowanie do tego zadania.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="7ac0a-159">- ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="7ac0a-159">-ContainerSettings</span></span>
<span data-ttu-id="7ac0a-160">Ustawienia kontenera, pod którym jest uruchamiane zadanie.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="7ac0a-161">Jeśli pula, która będzie uruchamiać to zadanie, ma ustawioną konfigurację containerConfiguration, również musi zostać ustawiona.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="7ac0a-162">Jeśli pula, która będzie uruchamiać to zadanie, nie ma ustawionej containerConfiguration, nie można tego ustawić.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="7ac0a-163">Gdy to określono, wszystkie katalogi rekurentywne poniżej AZ_BATCH_NODE_ROOT_DIR (katalogu głównego katalogów partii platformy Azure w węźle) są mapowane do kontenera, wszystkie zmienne środowiska zadania są mapowane do kontenera, a wiersz polecenia zadania jest wykonywany w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

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

### <span data-ttu-id="7ac0a-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac0a-164">-DefaultProfile</span></span>
<span data-ttu-id="7ac0a-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ac0a-166">- DependsOn</span><span class="sxs-lookup"><span data-stu-id="7ac0a-166">-DependsOn</span></span>
<span data-ttu-id="7ac0a-167">Określa, że zadanie zależy od innych zadań.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="7ac0a-168">Zadanie nie zostanie zaplanowane, dopóki wszystkie zadania zależne od tego nie zostaną pomyślnie ukończone.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="7ac0a-169">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="7ac0a-169">-DisplayName</span></span>
<span data-ttu-id="7ac0a-170">Określa nazwę wyświetlaną zadania.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="7ac0a-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="7ac0a-171">-EnvironmentSettings</span></span>
<span data-ttu-id="7ac0a-172">Określa ustawienia środowiska (jako pary klucz/wartość), które to polecenie cmdlet dodaje do zadania.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="7ac0a-173">Kluczem jest nazwa ustawienia środowiska.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-173">The key is the environment setting name.</span></span>
<span data-ttu-id="7ac0a-174">Wartość jest ustawieniem środowiska.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-174">The value is the environment setting.</span></span>

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

### <span data-ttu-id="7ac0a-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="7ac0a-175">-ExitConditions</span></span>
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

### <span data-ttu-id="7ac0a-176">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="7ac0a-176">-Id</span></span>
<span data-ttu-id="7ac0a-177">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="7ac0a-178">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="7ac0a-178">-Job</span></span>
<span data-ttu-id="7ac0a-179">Określa zadanie, w ramach którego to polecenie cmdlet tworzy zadanie.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="7ac0a-180">Aby uzyskać obiekt **PSCloudJob,** użyj Get-AzBatchJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="7ac0a-181">- JobId</span><span class="sxs-lookup"><span data-stu-id="7ac0a-181">-JobId</span></span>
<span data-ttu-id="7ac0a-182">Określa identyfikator zadania, na podstawie którego to polecenie cmdlet tworzy zadanie.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="7ac0a-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="7ac0a-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="7ac0a-184">Określa informacje o sposobu uruchamiania zadania wielo wystąpienie.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="7ac0a-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="7ac0a-185">-OutputFile</span></span>
<span data-ttu-id="7ac0a-186">Pobiera lub ustawia listę plików, które usługa Batch przekaże z węzła obliczeniowego po uruchomieniu wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="7ac0a-187">W przypadku zadań z wieloma wystąpieniami pliki będą przekazywane tylko z węzła obliczeniowego, w którym zostało wykonane zadanie podstawowe.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

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

### <span data-ttu-id="7ac0a-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="7ac0a-188">-ResourceFiles</span></span>
<span data-ttu-id="7ac0a-189">Określa pliki zasobów, jako pary klucz/wartość, których wymaga zadanie.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="7ac0a-190">Kluczem jest ścieżka pliku zasobu.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-190">The key is the resource file path.</span></span>
<span data-ttu-id="7ac0a-191">Wartość jest źródłem obiektów blob pliku zasobu.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-191">The value is the resource file blob source.</span></span>

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

### <span data-ttu-id="7ac0a-192">— Zadania</span><span class="sxs-lookup"><span data-stu-id="7ac0a-192">-Tasks</span></span>
<span data-ttu-id="7ac0a-193">Określa zbiór zadań do dodania.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="7ac0a-194">Każde zadanie musi mieć unikatowy identyfikator.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="7ac0a-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="7ac0a-195">-UserIdentity</span></span>
<span data-ttu-id="7ac0a-196">Tożsamość użytkownika, w ramach której zadanie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-196">The user identity under which the task runs.</span></span>

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

### <span data-ttu-id="7ac0a-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac0a-197">CommonParameters</span></span>
<span data-ttu-id="7ac0a-198">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac0a-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac0a-199">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ac0a-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac0a-200">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ac0a-200">INPUTS</span></span>

### <span data-ttu-id="7ac0a-201">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="7ac0a-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="7ac0a-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7ac0a-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7ac0a-203">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ac0a-203">OUTPUTS</span></span>

### <span data-ttu-id="7ac0a-204">System.Void</span><span class="sxs-lookup"><span data-stu-id="7ac0a-204">System.Void</span></span>

## <span data-ttu-id="7ac0a-205">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7ac0a-205">NOTES</span></span>

## <span data-ttu-id="7ac0a-206">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ac0a-206">RELATED LINKS</span></span>

[<span data-ttu-id="7ac0a-207">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7ac0a-207">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7ac0a-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="7ac0a-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="7ac0a-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7ac0a-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="7ac0a-210">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7ac0a-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="7ac0a-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7ac0a-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="7ac0a-212">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7ac0a-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="7ac0a-213">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="7ac0a-213">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
