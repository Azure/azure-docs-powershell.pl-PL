---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: 17d1c7c94726543aa30a032423576c8a7dcb6fcc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502308"
---
# <span data-ttu-id="2ac4d-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="2ac4d-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="2ac4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ac4d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac4d-103">Tworzy kontrolkę źródła automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="2ac4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ac4d-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ac4d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ac4d-105">DESCRIPTION</span></span>
<span data-ttu-id="2ac4d-106">Polecenie cmdlet New-AzAutomationSourceControl służy do tworzenia konfiguracji łączącej moje konto usługi Azure Automation z moim VSTS TFVC, VSTS Git lub GitHub.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="2ac4d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ac4d-107">EXAMPLES</span></span>

### <span data-ttu-id="2ac4d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ac4d-108">Example 1</span></span>
<span data-ttu-id="2ac4d-109">Utwórz konfigurację kontroli źródła, aby połączyć moje konto usługi Azure Automation z programem VSTS TFVC Project.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="2ac4d-110">Projekty TFVC nie mają oddziałów, dlatego nie określono parametru Branch.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://contoso.visualstudio.com/ContosoProduction/_versionControl" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://contoso.visualstudio.com/ContosoProduc...
```

### <span data-ttu-id="2ac4d-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2ac4d-111">Example 2</span></span>
<span data-ttu-id="2ac4d-112">Utwórz konfigurację kontroli źródła, aby połączyć moje konto usługi Azure Automation z moim VSTSm projektem git.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://contoso.visualstudio.com/_git/Finance" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://contoso.visualstudio.com/_git/Finan...
```

### <span data-ttu-id="2ac4d-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2ac4d-113">Example 3</span></span>
<span data-ttu-id="2ac4d-114">Utwórz konfigurację kontroli źródła, aby połączyć moje konto usługi Azure Automation z projektem GitHub.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "GitHub1" `
                                           -RepoUrl "https://github.com/Contoso/TestSourceControl.git" `
                                           -SourceType "GitHub" `
                                           -Branch "master" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name    SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------ ---------- -------- -------------- -------
GitHub1 GitHub     master /Runbooks  True     True           https://github.com/Contoso/TestSourceControl...
```

## <span data-ttu-id="2ac4d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ac4d-115">PARAMETERS</span></span>

### <span data-ttu-id="2ac4d-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="2ac4d-116">-AccessToken</span></span>
<span data-ttu-id="2ac4d-117">Token dostępu kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-117">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2ac4d-118">-AutomationAccountName</span></span>
<span data-ttu-id="2ac4d-119">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-119">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="2ac4d-120">-Branch</span></span>
<span data-ttu-id="2ac4d-121">Gałąź kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-121">The source control branch.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac4d-122">-DefaultProfile</span></span>
<span data-ttu-id="2ac4d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ac4d-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="2ac4d-124">-Description</span></span>
<span data-ttu-id="2ac4d-125">Opis kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-125">The source control description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="2ac4d-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="2ac4d-127">Właściwość publishRunbook kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="2ac4d-128">Jeśli DoNotPublishRunbook jest ustawiona, oznacza to, że elementy Runbook użytkownika będą importowane jako "wersja robocza".</span><span class="sxs-lookup"><span data-stu-id="2ac4d-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="2ac4d-129">-EnableAutoSync</span></span>
<span data-ttu-id="2ac4d-130">Właściwość ustawianiach dla kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-130">The autoSync property for the source control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="2ac4d-131">-FolderPath</span></span>
<span data-ttu-id="2ac4d-132">Ścieżka folderu kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-132">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2ac4d-133">-Name</span></span>
<span data-ttu-id="2ac4d-134">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-134">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-135">-Przelew</span><span class="sxs-lookup"><span data-stu-id="2ac4d-135">-RepoUrl</span></span>
<span data-ttu-id="2ac4d-136">Adres URL repozytorium kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-136">The source control repo url.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac4d-137">-ResourceGroupName</span></span>
<span data-ttu-id="2ac4d-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="2ac4d-139">-SourceType</span></span>
<span data-ttu-id="2ac4d-140">Typ kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-140">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ac4d-141">-Confirm</span></span>
<span data-ttu-id="2ac4d-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ac4d-143">-WhatIf</span></span>
<span data-ttu-id="2ac4d-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ac4d-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac4d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac4d-146">CommonParameters</span></span>
<span data-ttu-id="2ac4d-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac4d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac4d-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac4d-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac4d-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ac4d-149">INPUTS</span></span>

### <span data-ttu-id="2ac4d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac4d-150">System.String</span></span>

## <span data-ttu-id="2ac4d-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ac4d-151">OUTPUTS</span></span>

### <span data-ttu-id="2ac4d-152">Microsoft. Azure. Commands. Automation. model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="2ac4d-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="2ac4d-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ac4d-153">NOTES</span></span>

## <span data-ttu-id="2ac4d-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ac4d-154">RELATED LINKS</span></span>
