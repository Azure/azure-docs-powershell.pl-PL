---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 043e7bf24ce994edd0ce5621d2de8b17616d43f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502140"
---
# New-AzBatchTask

## STRESZCZENIe
Umożliwia utworzenie zadania wsadowego w ramach zadania.

## POLECENIA

### JobId_Single (domyślnie)
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

### JobId_Bulk
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Bulk
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Single
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

## Opis
Polecenie cmdlet **New-AzBatchTask** tworzy zadanie wsadowe platformy Azure w ramach zadania określonego przez parametr *JobID* lub parametr *zadania* .

## Przykłady

### Przykład 1. Tworzenie zadania wsadowego
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

To polecenie tworzy zadanie o IDENTYFIKATORze Task23 w ramach zadania o identyfikatorze Job ID-000001.
Zadanie uruchamia określone polecenie.
Użyj polecenia cmdlet **Get-AzBatchAccountKey** w celu przypisania kontekstu do zmiennej $Context.

### Przykład 2: Tworzenie zadania wsadowego
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze zadania w 000001, używając polecenia cmdlet **Get-AzBatchJob** .
Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.
Polecenie utworzy zadanie o IDENTYFIKATORze Task26 w ramach tego zadania.
Zadanie uruchamia określone polecenie, korzystając z podniesionych uprawnień.

### Przykład 3: Dodawanie kolekcji zadań do określonego zadania za pomocą potoku
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

Pierwsze polecenie tworzy odwołanie obiektu do kluczy konta dla konta wsadowego o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzBatchAccountKey**.
Polecenie zapisuje to odwołanie do obiektu w zmiennej $Context.
Następne dwa polecenia tworzą **PSCloudTask** obiekty za pomocą polecenia cmdlet New-Object.
Te polecenia przechowują zadania w zmiennych $Task 01 i $Task 02.
Polecenie ostatnie pobiera zadanie wsadowe o IDENTYFIKATORze Job-000001 przy użyciu polecenia **Get-AzBatchJob**.
Następnie polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.
Polecenie dodaje kolekcję zadań w ramach tego zadania.
Polecenie używa kontekstu przechowywanego w $Context.

### Przykład 4: Dodawanie zestawu zadań do określonego zadania
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

Pierwsze polecenie tworzy odwołanie obiektu do kluczy konta dla konta wsadowego o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzBatchAccountKey**.
Polecenie zapisuje to odwołanie do obiektu w zmiennej $Context.
Następne dwa polecenia tworzą **PSCloudTask** obiekty za pomocą polecenia cmdlet New-Object.
Te polecenia przechowują zadania w zmiennych $Task 01 i $Task 02.
Polecenie ostatnie umożliwia dodanie zadań przechowywanych w $Task 01 i $Task 02 w ramach zadania o identyfikatorze ID-000001.

### Przykład 5: Dodawanie zadania z plikami wyjściowymi
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### Przykład 6: Dodawanie zadania z ustawieniami tokenu uwierzytelniania
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### Przykład 7: Dodawanie zadania działającego w kontenerze
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## PARAMETRÓW

### -AffinityInformation
Określa wskazówkę o lokalizacji, której usługa wsadowa używa do zaznaczania węzła, na którym ma zostać uruchomione zadanie.

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

### -ApplicationPackageReferences
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

### -AuthenticationTokenSettings
Ustawienia tokenu uwierzytelniania, za pomocą którego zadanie może wykonywać operacje usługi wsadowej.
Jeśli to ustawienie jest skonfigurowane, usługa przetwarzania wsadowego dostarcza zadanie z tokenem uwierzytelniania, którego można użyć do uwierzytelniania operacji usługi przetwarzania wsadowego bez konieczności korzystania z klucza dostępu do konta. Token jest dostarczany za pośrednictwem zmiennej środowiskowej AZ_BATCH_AUTHENTICATION_TOKEN. Operacje, które mogą być wykonywane przez zadanie przy użyciu tokenu, zależą od ustawień. Na przykład zadanie może zażądać uprawnień do zadania, aby można było dodać do zadania inne zadania lub sprawdzić stan zadania lub innych zadań.

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

### -BatchContext
Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.
Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego. Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu. W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu. Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.

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

### -CommandLine
Określa wiersz polecenia dla zadania.

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

### -Ograniczenia
Określa ograniczenia wykonania dotyczące tego zadania.

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

### -ContainerSettings
Ustawienia kontenera, w którym jest uruchamiane zadanie.
Jeśli Pula, która będzie uruchamiać to zadanie, ma ustawiony containerConfiguration, należy ją również ustawić. Jeśli Pula, która będzie uruchamiać to zadanie, nie ma ustawionego zestawu containerConfiguration, nie może być ustawiona. Jeśli ta funkcja jest określona, wszystkie katalogi rekursywnie poniżej AZ_BATCH_NODE_ROOT_DIR (katalog główny katalogów usługi Azure Batch w węźle) są mapowane na kontener, wszystkie zmienne środowiskowe zadań są mapowane na kontener, a wiersz polecenia zadanie jest wykonywany w kontenerze.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -DependsOn
Określa, że zadanie zależy od innych zadań.
Zadanie nie zostanie zaplanowane, dopóki wszystkie zadania zależne od siebie nie zostaną pomyślnie ukończone.

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

### -DisplayName
Określa nazwę wyświetlaną zadania.

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

### -EnvironmentSettings
Określa ustawienia środowiska jako pary klucz/wartość, które to polecenie cmdlet dodaje do zadania.
Klucz jest nazwą ustawienia środowiska.
Wartość to ustawienie środowiska.

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

### -ExitConditions
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

### -ID
Określa identyfikator zadania.

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

### — Zadanie
Określa zadanie, za pomocą którego to polecenie cmdlet tworzy zadanie.
Aby uzyskać obiekt **PSCloudJob** , użyj polecenia cmdlet Get-AzBatchJob.

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

### -JobId
Określa identyfikator zadania, za pomocą którego to polecenie cmdlet tworzy zadanie.

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

### -MultiInstanceSettings
Określa informacje dotyczące uruchamiania zadania o wielu wystąpieniach.

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

### -Plik_wyjściowy
Pobiera lub ustawia listę plików, które usługa wsadowa przekaże z węzła obliczeniowego po uruchomieniu wiersza polecenia.
W przypadku zadań o wielu wystąpieniach pliki będą przekazywane tylko z węzła obliczeniowego, na którym jest wykonywane zadanie główne.

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

### -ResourceFiles
Określa pliki zasobów, takie jak pary klucz/wartość, których wymaga zadanie.
Klucz to ścieżka pliku zasobu.
Wartość to źródło obiektów blob pliku zasobów.

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

### -Zadania
Określa kolekcję zadań, które mają zostać dodane.
Każde zadanie musi mieć unikatowy identyfikator.

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

### -UserIdentity
Tożsamość użytkownika, pod którą jest uruchamiane zadanie.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft.Azure.Commands.Batch. Modele. PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## WYSYŁA

### System. void

## INFORMACYJN

## LINKI POKREWNE

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Get-AzBatchTask](./Get-AzBatchTask.md)

[Nowe — AzBatchTask](./New-AzBatchTask.md)

[Remove-AzBatchTask](./Remove-AzBatchTask.md)

[Zatrzymaj — AzBatchTask](./Stop-AzBatchTask.md)

[Polecenia cmdlet usługi Azure Batch](/powershell/module/Az.Batch/)
