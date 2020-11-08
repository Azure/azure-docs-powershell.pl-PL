---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: ed10bd42fb52515cb05adadfc69ee4f1620150e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053935"
---
# <span data-ttu-id="9b6c1-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="9b6c1-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="9b6c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b6c1-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6c1-103">Regeneruje klucze rejestracji dla konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9b6c1-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="9b6c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b6c1-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b6c1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9b6c1-105">DESCRIPTION</span></span>
<span data-ttu-id="9b6c1-106">Polecenie cmdlet **New-AzAutomationKey** generuje klucze rejestracji dla konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9b6c1-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="9b6c1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b6c1-107">EXAMPLES</span></span>

### <span data-ttu-id="9b6c1-108">Przykład 1. Regeneruj klucz dla konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="9b6c1-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9b6c1-109">To polecenie generuje klucz podstawowy dla konta usługi Azure Automation o nazwie AutomationAccount01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="9b6c1-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="9b6c1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b6c1-110">PARAMETERS</span></span>

### <span data-ttu-id="9b6c1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9b6c1-111">-AutomationAccountName</span></span>
<span data-ttu-id="9b6c1-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet ponownie generuje klucze.</span><span class="sxs-lookup"><span data-stu-id="9b6c1-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="9b6c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6c1-113">-DefaultProfile</span></span>
<span data-ttu-id="9b6c1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9b6c1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b6c1-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="9b6c1-115">-KeyType</span></span>
<span data-ttu-id="9b6c1-116">Określa typ klucza rejestracji agenta.</span><span class="sxs-lookup"><span data-stu-id="9b6c1-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="9b6c1-117">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="9b6c1-117">Valid values are:</span></span> 
- <span data-ttu-id="9b6c1-118">Początkowe</span><span class="sxs-lookup"><span data-stu-id="9b6c1-118">Primary</span></span> 
- <span data-ttu-id="9b6c1-119">Dodatkowej</span><span class="sxs-lookup"><span data-stu-id="9b6c1-119">Secondary</span></span>

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

### <span data-ttu-id="9b6c1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b6c1-120">-ResourceGroupName</span></span>
<span data-ttu-id="9b6c1-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b6c1-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9b6c1-122">To polecenie cmdlet ponownie generuje klucze dla konta automatyzacji w grupie zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9b6c1-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b6c1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6c1-123">CommonParameters</span></span>
<span data-ttu-id="9b6c1-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b6c1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6c1-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b6c1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6c1-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b6c1-126">INPUTS</span></span>

### <span data-ttu-id="9b6c1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9b6c1-127">System.String</span></span>

## <span data-ttu-id="9b6c1-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b6c1-128">OUTPUTS</span></span>

### <span data-ttu-id="9b6c1-129">Microsoft. Azure. Commands. Automation. model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="9b6c1-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="9b6c1-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b6c1-130">NOTES</span></span>

## <span data-ttu-id="9b6c1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b6c1-131">RELATED LINKS</span></span>
