---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/update-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
ms.openlocfilehash: 7786431232f9570557593d2fbdde65a21e34f9bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710444"
---
# <span data-ttu-id="fd62a-101">Update-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="fd62a-101">Update-AzAutomationSourceControl</span></span>

## <span data-ttu-id="fd62a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd62a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd62a-103">Aktualizuje kontrolę źródła usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="fd62a-103">Updates an Azure Automation source control.</span></span>

## <span data-ttu-id="fd62a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd62a-104">SYNTAX</span></span>

```
Update-AzAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd62a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd62a-105">DESCRIPTION</span></span>
<span data-ttu-id="fd62a-106">Polecenie cmdlet Update-AzAutomationSourceControl modyfikuje wartość pola w kontroli źródła w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="fd62a-106">The Update-AzAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="fd62a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd62a-107">EXAMPLES</span></span>

### <span data-ttu-id="fd62a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd62a-108">Example 1</span></span>
<span data-ttu-id="fd62a-109">To polecenie ustawia wartość FAŁSZ pola PublishRunbook dla kontroli źródła usługi Azure Automation o nazwie VSTSNative na koncie o nazwie devAccount.</span><span class="sxs-lookup"><span data-stu-id="fd62a-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="fd62a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd62a-110">PARAMETERS</span></span>

### <span data-ttu-id="fd62a-111">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="fd62a-111">-AccessToken</span></span>
<span data-ttu-id="fd62a-112">Token dostępu kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="fd62a-112">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fd62a-113">-AutomationAccountName</span></span>
<span data-ttu-id="fd62a-114">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="fd62a-114">The automation account name.</span></span>

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

### <span data-ttu-id="fd62a-115">-Ustawianiach</span><span class="sxs-lookup"><span data-stu-id="fd62a-115">-AutoSync</span></span>
<span data-ttu-id="fd62a-116">Właściwość ustawianiach dla kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="fd62a-116">The autoSync property for the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-117">-Branch</span><span class="sxs-lookup"><span data-stu-id="fd62a-117">-Branch</span></span>
<span data-ttu-id="fd62a-118">Gałąź kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="fd62a-118">The source control branch.</span></span>

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

### <span data-ttu-id="fd62a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd62a-119">-DefaultProfile</span></span>
<span data-ttu-id="fd62a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd62a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd62a-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="fd62a-121">-Description</span></span>
<span data-ttu-id="fd62a-122">Opis kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="fd62a-122">The source control description.</span></span>

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

### <span data-ttu-id="fd62a-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="fd62a-123">-FolderPath</span></span>
<span data-ttu-id="fd62a-124">Ścieżka folderu kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="fd62a-124">The source control folder path.</span></span>

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

### <span data-ttu-id="fd62a-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd62a-125">-Name</span></span>
<span data-ttu-id="fd62a-126">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="fd62a-126">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-127">-PublishRunbook</span><span class="sxs-lookup"><span data-stu-id="fd62a-127">-PublishRunbook</span></span>
<span data-ttu-id="fd62a-128">Właściwość publishRunbook kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="fd62a-128">The publishRunbook property of the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd62a-129">-ResourceGroupName</span></span>
<span data-ttu-id="fd62a-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd62a-130">The resource group name.</span></span>

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

### <span data-ttu-id="fd62a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd62a-131">-Confirm</span></span>
<span data-ttu-id="fd62a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd62a-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd62a-133">-WhatIf</span></span>
<span data-ttu-id="fd62a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd62a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd62a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd62a-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd62a-136">CommonParameters</span></span>
<span data-ttu-id="fd62a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd62a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd62a-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd62a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd62a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd62a-139">INPUTS</span></span>

### <span data-ttu-id="fd62a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fd62a-140">System.String</span></span>

## <span data-ttu-id="fd62a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd62a-141">OUTPUTS</span></span>

### <span data-ttu-id="fd62a-142">Microsoft. Azure. Commands. Automation. model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="fd62a-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="fd62a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd62a-143">NOTES</span></span>

## <span data-ttu-id="fd62a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd62a-144">RELATED LINKS</span></span>
