---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/update-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Update-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Update-AzureRmAutomationSourceControl.md
ms.openlocfilehash: 78308306e7bc46d4a9b3fadf4b00050cf9898f26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718386"
---
# <span data-ttu-id="aaad6-101">Update-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="aaad6-101">Update-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="aaad6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aaad6-102">SYNOPSIS</span></span>
<span data-ttu-id="aaad6-103">Aktualizuje kontrolę źródła usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="aaad6-103">Updates an Azure Automation source control.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaad6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aaad6-104">SYNTAX</span></span>

```
Update-AzureRmAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaad6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aaad6-105">DESCRIPTION</span></span>
<span data-ttu-id="aaad6-106">Polecenie cmdlet Update-AzureRmAutomationSourceControl modyfikuje wartość pola w kontroli źródła w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="aaad6-106">The Update-AzureRmAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="aaad6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aaad6-107">EXAMPLES</span></span>

### <span data-ttu-id="aaad6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aaad6-108">Example 1</span></span>
<span data-ttu-id="aaad6-109">To polecenie ustawia wartość FAŁSZ pola PublishRunbook dla kontroli źródła usługi Azure Automation o nazwie VSTSNative na koncie o nazwie devAccount.</span><span class="sxs-lookup"><span data-stu-id="aaad6-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="aaad6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aaad6-110">PARAMETERS</span></span>

### <span data-ttu-id="aaad6-111">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="aaad6-111">-AccessToken</span></span>
<span data-ttu-id="aaad6-112">Token dostępu kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="aaad6-112">The source control access token.</span></span>

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

### <span data-ttu-id="aaad6-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aaad6-113">-AutomationAccountName</span></span>
<span data-ttu-id="aaad6-114">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="aaad6-114">The automation account name.</span></span>

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

### <span data-ttu-id="aaad6-115">-Ustawianiach</span><span class="sxs-lookup"><span data-stu-id="aaad6-115">-AutoSync</span></span>
<span data-ttu-id="aaad6-116">Właściwość ustawianiach dla kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="aaad6-116">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="aaad6-117">-Branch</span><span class="sxs-lookup"><span data-stu-id="aaad6-117">-Branch</span></span>
<span data-ttu-id="aaad6-118">Gałąź kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="aaad6-118">The source control branch.</span></span>

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

### <span data-ttu-id="aaad6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaad6-119">-DefaultProfile</span></span>
<span data-ttu-id="aaad6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aaad6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaad6-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="aaad6-121">-Description</span></span>
<span data-ttu-id="aaad6-122">Opis kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="aaad6-122">The source control description.</span></span>

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

### <span data-ttu-id="aaad6-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="aaad6-123">-FolderPath</span></span>
<span data-ttu-id="aaad6-124">Ścieżka folderu kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="aaad6-124">The source control folder path.</span></span>

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

### <span data-ttu-id="aaad6-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aaad6-125">-Name</span></span>
<span data-ttu-id="aaad6-126">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="aaad6-126">The source control name.</span></span>

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

### <span data-ttu-id="aaad6-127">-PublishRunbook</span><span class="sxs-lookup"><span data-stu-id="aaad6-127">-PublishRunbook</span></span>
<span data-ttu-id="aaad6-128">Właściwość publishRunbook kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="aaad6-128">The publishRunbook property of the source control.</span></span>

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

### <span data-ttu-id="aaad6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaad6-129">-ResourceGroupName</span></span>
<span data-ttu-id="aaad6-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aaad6-130">The resource group name.</span></span>

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

### <span data-ttu-id="aaad6-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aaad6-131">-Confirm</span></span>
<span data-ttu-id="aaad6-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaad6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaad6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaad6-133">-WhatIf</span></span>
<span data-ttu-id="aaad6-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaad6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaad6-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aaad6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaad6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaad6-136">CommonParameters</span></span>
<span data-ttu-id="aaad6-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaad6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaad6-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaad6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaad6-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aaad6-139">INPUTS</span></span>

### <span data-ttu-id="aaad6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="aaad6-140">System.String</span></span>

## <span data-ttu-id="aaad6-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aaad6-141">OUTPUTS</span></span>

### <span data-ttu-id="aaad6-142">Microsoft. Azure. Commands. Automation. model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="aaad6-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="aaad6-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aaad6-143">NOTES</span></span>

## <span data-ttu-id="aaad6-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aaad6-144">RELATED LINKS</span></span>
