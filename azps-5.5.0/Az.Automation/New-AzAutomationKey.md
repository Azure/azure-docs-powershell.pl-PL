---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: ed10bd42fb52515cb05adadfc69ee4f1620150e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201067"
---
# <span data-ttu-id="4ea86-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="4ea86-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="4ea86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ea86-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea86-103">Ponownie generuje klucze rejestracji dla konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4ea86-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="4ea86-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4ea86-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ea86-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4ea86-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea86-106">Polecenie **cmdlet New-AzAutomationKey** ponownie generuje klucze rejestracji dla konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4ea86-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="4ea86-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4ea86-107">EXAMPLES</span></span>

### <span data-ttu-id="4ea86-108">Przykład 1. Ponowne generowanie klucza dla konta automatyzacji</span><span class="sxs-lookup"><span data-stu-id="4ea86-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="4ea86-109">To polecenie ponownie generuje klucz podstawowy dla konta automatyzacji Azure o nazwie AutomationAccount01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4ea86-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="4ea86-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ea86-110">PARAMETERS</span></span>

### <span data-ttu-id="4ea86-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4ea86-111">-AutomationAccountName</span></span>
<span data-ttu-id="4ea86-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet ponownie generuje klucze.</span><span class="sxs-lookup"><span data-stu-id="4ea86-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="4ea86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea86-113">-DefaultProfile</span></span>
<span data-ttu-id="4ea86-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4ea86-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ea86-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4ea86-115">-KeyType</span></span>
<span data-ttu-id="4ea86-116">Określa typ klucza rejestracji agenta.</span><span class="sxs-lookup"><span data-stu-id="4ea86-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="4ea86-117">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="4ea86-117">Valid values are:</span></span> 
- <span data-ttu-id="4ea86-118">Podstawowa</span><span class="sxs-lookup"><span data-stu-id="4ea86-118">Primary</span></span> 
- <span data-ttu-id="4ea86-119">Pomocniczy</span><span class="sxs-lookup"><span data-stu-id="4ea86-119">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea86-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea86-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ea86-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ea86-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4ea86-122">To polecenie cmdlet ponownie generuje klucze dla konta automatyzacji w grupie zasobów, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4ea86-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ea86-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea86-123">CommonParameters</span></span>
<span data-ttu-id="4ea86-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea86-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea86-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ea86-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea86-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ea86-126">INPUTS</span></span>

### <span data-ttu-id="4ea86-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4ea86-127">System.String</span></span>

## <span data-ttu-id="4ea86-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ea86-128">OUTPUTS</span></span>

### <span data-ttu-id="4ea86-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="4ea86-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="4ea86-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4ea86-130">NOTES</span></span>

## <span data-ttu-id="4ea86-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ea86-131">RELATED LINKS</span></span>
