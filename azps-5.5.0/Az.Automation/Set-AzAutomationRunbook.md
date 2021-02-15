---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182122"
---
# <span data-ttu-id="ed985-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed985-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="ed985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed985-102">SYNOPSIS</span></span>
<span data-ttu-id="ed985-103">Modyfikuje podręcznik.</span><span class="sxs-lookup"><span data-stu-id="ed985-103">Modifies a runbook.</span></span>

## <span data-ttu-id="ed985-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed985-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed985-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed985-105">DESCRIPTION</span></span>
<span data-ttu-id="ed985-106">Polecenie **cmdlet Set-AzAutomationRunbook** modyfikuje konfigurację podręcznika azure automation w usłudze APS.</span><span class="sxs-lookup"><span data-stu-id="ed985-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="ed985-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed985-107">EXAMPLES</span></span>

### <span data-ttu-id="ed985-108">Przykład 1. Włączanie szczegółowego rejestrowania dla podręcznika uruchamiania</span><span class="sxs-lookup"><span data-stu-id="ed985-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ed985-109">To polecenie umożliwia szczegółowe rejestrowanie zadań określonego podręcznika na koncie automatyzacji platformy Azure o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ed985-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ed985-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed985-110">PARAMETERS</span></span>

### <span data-ttu-id="ed985-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ed985-111">-AutomationAccountName</span></span>
<span data-ttu-id="ed985-112">Określa nazwę konta automatyzacji, na którym to polecenie cmdlet modyfikuje zestaw runbook.</span><span class="sxs-lookup"><span data-stu-id="ed985-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="ed985-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed985-113">-DefaultProfile</span></span>
<span data-ttu-id="ed985-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ed985-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed985-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="ed985-115">-Description</span></span>
<span data-ttu-id="ed985-116">Określa opis podręcznika.</span><span class="sxs-lookup"><span data-stu-id="ed985-116">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed985-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="ed985-117">-LogProgress</span></span>
<span data-ttu-id="ed985-118">Określa, czy dzienniki dziennika uruchamiania mają być postępowe.</span><span class="sxs-lookup"><span data-stu-id="ed985-118">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed985-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="ed985-119">-LogVerbose</span></span>
<span data-ttu-id="ed985-120">Określa, czy rejestrowanie zawiera szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="ed985-120">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed985-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ed985-121">-Name</span></span>
<span data-ttu-id="ed985-122">Określa nazwę podręcznika, który ma być zmieniany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed985-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed985-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed985-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed985-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje zestaw runbook.</span><span class="sxs-lookup"><span data-stu-id="ed985-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="ed985-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="ed985-125">-Tag</span></span>
<span data-ttu-id="ed985-126">Tagi podręcznika.</span><span class="sxs-lookup"><span data-stu-id="ed985-126">The runbook tags.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed985-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed985-127">CommonParameters</span></span>
<span data-ttu-id="ed985-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed985-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed985-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed985-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed985-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed985-130">INPUTS</span></span>

### <span data-ttu-id="ed985-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ed985-131">System.String</span></span>

### <span data-ttu-id="ed985-132">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="ed985-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="ed985-133">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ed985-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ed985-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed985-134">OUTPUTS</span></span>

### <span data-ttu-id="ed985-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="ed985-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="ed985-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed985-136">NOTES</span></span>

## <span data-ttu-id="ed985-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed985-137">RELATED LINKS</span></span>

[<span data-ttu-id="ed985-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed985-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="ed985-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed985-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="ed985-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed985-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="ed985-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed985-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ed985-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed985-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ed985-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed985-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="ed985-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed985-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="ed985-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed985-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


