---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: d9fbbed1beb67ce1bc8732cb5641c78705fd6a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956497"
---
# <span data-ttu-id="f9375-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="f9375-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="f9375-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9375-102">SYNOPSIS</span></span>
<span data-ttu-id="f9375-103">Tworzy kontrolkę źródła automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f9375-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="f9375-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f9375-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9375-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f9375-105">DESCRIPTION</span></span>
<span data-ttu-id="f9375-106">Polecenie New-AzAutomationSourceControl tworzy konfigurację w celu połączenia konta usługi Azure Automation z moim poleceniem VSTS TFVC, VSTS Git lub GitHub.</span><span class="sxs-lookup"><span data-stu-id="f9375-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="f9375-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f9375-107">EXAMPLES</span></span>

### <span data-ttu-id="f9375-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9375-108">Example 1</span></span>
<span data-ttu-id="f9375-109">Utwórz konfigurację kontrolki źródła, aby połączyć moje konto usługi Azure Automation z moim projektem VSTS TFVC.</span><span class="sxs-lookup"><span data-stu-id="f9375-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="f9375-110">Projekty TFVC nie mają gałęzi, dlatego parametr Branch nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="f9375-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://dev.azure.com/<accountname>/<adoprojectname>/_git/<repositoryname>" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://dev.azure.com/<accountname>/<adopro...
```

### <span data-ttu-id="f9375-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f9375-111">Example 2</span></span>
<span data-ttu-id="f9375-112">Utwórz konfigurację kontrolki źródła, aby połączyć moje konto usługi Azure Automation z projektem VSTS Git.</span><span class="sxs-lookup"><span data-stu-id="f9375-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://dev.azure.com/<accountname>/<adoprojectname>/_git/<repositoryname>" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://dev.azure.com/<accountname>/<adopro...
```

### <span data-ttu-id="f9375-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f9375-113">Example 3</span></span>
<span data-ttu-id="f9375-114">Utwórz konfigurację kontrolki źródła, aby połączyć moje konto usługi Azure Automation z projektem GitHub.</span><span class="sxs-lookup"><span data-stu-id="f9375-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


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

## <span data-ttu-id="f9375-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9375-115">PARAMETERS</span></span>

### <span data-ttu-id="f9375-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="f9375-116">-AccessToken</span></span>
<span data-ttu-id="f9375-117">Token dostępu kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="f9375-117">The source control access token.</span></span>

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

### <span data-ttu-id="f9375-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f9375-118">-AutomationAccountName</span></span>
<span data-ttu-id="f9375-119">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f9375-119">The automation account name.</span></span>

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

### <span data-ttu-id="f9375-120">— Gałąź</span><span class="sxs-lookup"><span data-stu-id="f9375-120">-Branch</span></span>
<span data-ttu-id="f9375-121">Gałąź kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="f9375-121">The source control branch.</span></span>

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

### <span data-ttu-id="f9375-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9375-122">-DefaultProfile</span></span>
<span data-ttu-id="f9375-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9375-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9375-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="f9375-124">-Description</span></span>
<span data-ttu-id="f9375-125">Opis kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="f9375-125">The source control description.</span></span>

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

### <span data-ttu-id="f9375-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="f9375-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="f9375-127">Właściwość publishRunbook kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="f9375-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="f9375-128">Jeśli jest ustawiony obiekt DoNotPublishRunbook, oznacza to, że podręczniki użytkownika zostaną zaimportowane jako "Wersja robocza".</span><span class="sxs-lookup"><span data-stu-id="f9375-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

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

### <span data-ttu-id="f9375-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="f9375-129">-EnableAutoSync</span></span>
<span data-ttu-id="f9375-130">Właściwość autoSync kontrolki źródłowej.</span><span class="sxs-lookup"><span data-stu-id="f9375-130">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="f9375-131">- FolderPath</span><span class="sxs-lookup"><span data-stu-id="f9375-131">-FolderPath</span></span>
<span data-ttu-id="f9375-132">Ścieżka folderu kontrolki źródłowej.</span><span class="sxs-lookup"><span data-stu-id="f9375-132">The source control folder path.</span></span>

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

### <span data-ttu-id="f9375-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f9375-133">-Name</span></span>
<span data-ttu-id="f9375-134">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="f9375-134">The source control name.</span></span>

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

### <span data-ttu-id="f9375-135">-RepoUrl</span><span class="sxs-lookup"><span data-stu-id="f9375-135">-RepoUrl</span></span>
<span data-ttu-id="f9375-136">Adres URL ponownego adresu url kontrolki źródłowej.</span><span class="sxs-lookup"><span data-stu-id="f9375-136">The source control repo url.</span></span>

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

### <span data-ttu-id="f9375-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9375-137">-ResourceGroupName</span></span>
<span data-ttu-id="f9375-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9375-138">The resource group name.</span></span>

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

### <span data-ttu-id="f9375-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="f9375-139">-SourceType</span></span>
<span data-ttu-id="f9375-140">Typ kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="f9375-140">The source control type.</span></span>

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

### <span data-ttu-id="f9375-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9375-141">-Confirm</span></span>
<span data-ttu-id="f9375-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f9375-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9375-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9375-143">-WhatIf</span></span>
<span data-ttu-id="f9375-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9375-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9375-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f9375-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9375-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9375-146">CommonParameters</span></span>
<span data-ttu-id="f9375-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9375-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9375-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9375-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9375-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9375-149">INPUTS</span></span>

### <span data-ttu-id="f9375-150">System.String</span><span class="sxs-lookup"><span data-stu-id="f9375-150">System.String</span></span>

## <span data-ttu-id="f9375-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9375-151">OUTPUTS</span></span>

### <span data-ttu-id="f9375-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="f9375-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="f9375-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f9375-153">NOTES</span></span>

## <span data-ttu-id="f9375-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9375-154">RELATED LINKS</span></span>
