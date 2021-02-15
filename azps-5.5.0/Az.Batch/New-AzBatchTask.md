---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 043e7bf24ce994edd0ce5621d2de8b17616d43f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197019"
---
# New-AzBatchTask

## SYNOPSIS
Tworzy zadanie wsadowe w obszarze zadania.

## SKŁADNIA

### JobId_Single (domyślne)
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

## OPIS
Polecenie **cmdlet New-AzBatchTask** tworzy zadanie usługi Azure Batch w ramach zadania określonego przez parametr *JobId* lub *parametr Job.*

## PRZYKŁADY

### Przykład 1. Tworzenie zadania wsadowego
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

To polecenie tworzy zadanie o identyfikatorze Zadanie23 w ramach zadania o identyfikatorze Zadanie 000001.
Zadanie zostanie uruchamiane zgodnie z określonym poleceniem.
Użyj polecenia **cmdlet Get-AzBatchAccountKey,** aby przypisać kontekst do zmiennej $Context danych.

### Przykład 2. Tworzenie zadania wsadowego
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

To polecenie pobiera zadanie Batch o identyfikatorze Zadanie-000001 przy użyciu polecenia cmdlet **Get-AzBatchJob.**
Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet przy użyciu operatora potoku.
To polecenie tworzy zadanie o identyfikatorze Zadanie26 w ramach tego zadania.
Zadanie jest uruchamiane za pomocą określonego polecenia z podwyższonym poziomem uprawnień.

### Przykład 3. Dodawanie zbioru zadań do określonego zadania przy użyciu potoku
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

Pierwsze polecenie tworzy odwołanie do obiektu do kluczy konta dla konta wsadowego o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzBatchAccountKey.**
Polecenie przechowuje to odwołanie do obiektu w $Context zmienną.
Następne dwa polecenia tworzą **obiekty PSCloudTask** przy użyciu New-Object cmdlet.
Polecenia przechowują zadania w zmiennych $Task 01 i $Task 02.
Końcowe polecenie otrzymuje zadanie Batch o identyfikatorze Zadanie-000001 przy użyciu polecenia **Get-AzBatchJob.**
Następnie polecenie przekazuje to zadanie do bieżącego polecenia cmdlet przy użyciu operatora potoku.
To polecenie powoduje dodanie kolekcji zadań w ramach tego zadania.
To polecenie używa kontekstu przechowywanego w $Context.

### Przykład 4. Dodawanie kolekcji zadań do określonego zadania
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

Pierwsze polecenie tworzy odwołanie do obiektu do kluczy konta dla konta wsadowego o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzBatchAccountKey.**
Polecenie przechowuje to odwołanie do obiektu w $Context zmienną.
Następne dwa polecenia tworzą **obiekty PSCloudTask** przy użyciu New-Object cmdlet.
Polecenia przechowują zadania w zmiennych $Task 01 i $Task 02.
Ostatnie polecenie powoduje dodanie zadań przechowywanych w $Task 01 i $Task 02 pod zadaniem o identyfikatorze Zadanie 000001.

### Przykład 5. Dodawanie zadania z plikami wyjściowmi
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### Przykład 6. Dodawanie zadania z ustawieniami tokenu uwierzytelniania
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### Przykład 7. Dodawanie zadania uruchamianego w kontenerze
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## PARAMETERS

### -AffinityInformation
Określa wskazówkę lokalizacji używaną przez usługę Batch do wybierania węzła, w którym ma być uruchamiane zadanie.

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

### —AuthenticationTokenSettings
Ustawienia tokenu uwierzytelniania, za pomocą których zadanie może wykonywać operacje usługi wsadowej.
Jeśli ta wartość jest ustawiona, usługa wsadowa udostępnia zadanie z tokenem uwierzytelniania, który może być używany do uwierzytelniania operacji usługi wsadowej bez konieczności użycia klucza dostępu do konta. Token jest dostarczany za pośrednictwem AZ_BATCH_AUTHENTICATION_TOKEN środowiskowej. Operacje, które zadanie może wykonać przy użyciu tokenu, zależą od ustawień. Na przykład zadanie może zażądać uprawnień zadań w celu dodania innych zadań do zadania lub sprawdzić stan zadania lub innych zadań.

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

### - BatchContext
Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.
Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory. Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu. Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany. Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.

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

### —CommandLine
Określa wiersz polecenia zadania.

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

### — Ograniczenia
Określa ograniczenia wykonywania, które mają zastosowanie do tego zadania.

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

### - ContainerSettings
Ustawienia kontenera, pod którym jest uruchamiane zadanie.
Jeśli pula, która będzie uruchamiać to zadanie, ma ustawioną konfigurację containerConfiguration, również musi zostać ustawiona. Jeśli pula, która będzie uruchamiać to zadanie, nie ma ustawionej containerConfiguration, nie można tego ustawić. Gdy to określono, wszystkie katalogi rekurentywne poniżej AZ_BATCH_NODE_ROOT_DIR (katalogu głównego katalogów partii platformy Azure w węźle) są mapowane do kontenera, wszystkie zmienne środowiska zadań są mapowane do kontenera, a wiersz polecenia zadania jest wykonywany w kontenerze.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### - DependsOn
Określa, że zadanie zależy od innych zadań.
Zadanie nie zostanie zaplanowane, dopóki wszystkie zadania zależne od systemu nie zostaną pomyślnie ukończone.

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

### — DisplayName
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
Określa ustawienia środowiska (jako pary klucz/wartość), które to polecenie cmdlet dodaje do zadania.
Kluczem jest nazwa ustawienia środowiska.
Wartość jest ustawieniem środowiska.

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

### — Identyfikator
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
Określa zadanie, w ramach którego to polecenie cmdlet tworzy zadanie.
Aby uzyskać obiekt **PSCloudJob,** użyj Get-AzBatchJob cmdlet.

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

### - JobId
Określa identyfikator zadania, pod którym to polecenie cmdlet tworzy zadanie.

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
Określa informacje o sposobu uruchamiania zadania wielo wystąpienie.

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

### -OutputFile
Pobiera lub ustawia listę plików, które usługa Batch przekaże z węzła obliczeniowego po uruchomieniu wiersza polecenia.
W przypadku zadań z wieloma wystąpieniami pliki będą przekazywane tylko z węzła obliczeniowego, w którym zostało wykonane zadanie podstawowe.

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
Określa pliki zasobów jako pary klucz/wartość, których wymaga zadanie.
Kluczem jest ścieżka pliku zasobu.
Wartość jest źródłem obiektów blob pliku zasobu.

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

### — Zadania
Określa zbiór zadań do dodania.
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
Tożsamość użytkownika, w ramach której zadanie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Batch. Models.PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## DANE WYJŚCIOWE

### System.Void

## NOTATKI

## LINKI POKREWNE

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Get-AzBatchTask](./Get-AzBatchTask.md)

[New-AzBatchTask](./New-AzBatchTask.md)

[Remove-AzBatchTask](./Remove-AzBatchTask.md)

[Stop-AzBatchTask](./Stop-AzBatchTask.md)

[Polecenia cmdlet partii platformy Azure](/powershell/module/Az.Batch/)
