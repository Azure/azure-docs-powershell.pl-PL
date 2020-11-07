---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: 1d0587ae9d1d45de4f08b71baa48ebb5e1633a36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710534"
---
# <span data-ttu-id="d8b80-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="d8b80-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="d8b80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8b80-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b80-103">Regeneruje klucze rejestracji dla konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d8b80-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="d8b80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8b80-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8b80-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8b80-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b80-106">Polecenie cmdlet **New-AzAutomationKey** generuje klucze rejestracji dla konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d8b80-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="d8b80-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8b80-107">EXAMPLES</span></span>

### <span data-ttu-id="d8b80-108">Przykład 1. Regeneruj klucz dla konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="d8b80-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="d8b80-109">To polecenie generuje klucz podstawowy dla konta usługi Azure Automation o nazwie AutomationAccount01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d8b80-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="d8b80-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8b80-110">PARAMETERS</span></span>

### <span data-ttu-id="d8b80-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8b80-111">-AutomationAccountName</span></span>
<span data-ttu-id="d8b80-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet ponownie generuje klucze.</span><span class="sxs-lookup"><span data-stu-id="d8b80-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="d8b80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b80-113">-DefaultProfile</span></span>
<span data-ttu-id="d8b80-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d8b80-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8b80-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d8b80-115">-KeyType</span></span>
<span data-ttu-id="d8b80-116">Określa typ klucza rejestracji agenta.</span><span class="sxs-lookup"><span data-stu-id="d8b80-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="d8b80-117">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="d8b80-117">Valid values are:</span></span> 
- <span data-ttu-id="d8b80-118">Początkowe</span><span class="sxs-lookup"><span data-stu-id="d8b80-118">Primary</span></span> 
- <span data-ttu-id="d8b80-119">Dodatkowej</span><span class="sxs-lookup"><span data-stu-id="d8b80-119">Secondary</span></span>

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

### <span data-ttu-id="d8b80-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b80-120">-ResourceGroupName</span></span>
<span data-ttu-id="d8b80-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8b80-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d8b80-122">To polecenie cmdlet ponownie generuje klucze dla konta automatyzacji w grupie zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d8b80-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8b80-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b80-123">CommonParameters</span></span>
<span data-ttu-id="d8b80-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b80-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b80-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b80-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b80-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8b80-126">INPUTS</span></span>

### <span data-ttu-id="d8b80-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d8b80-127">System.String</span></span>

## <span data-ttu-id="d8b80-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8b80-128">OUTPUTS</span></span>

### <span data-ttu-id="d8b80-129">Microsoft. Azure. Commands. Automation. model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="d8b80-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="d8b80-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8b80-130">NOTES</span></span>

## <span data-ttu-id="d8b80-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8b80-131">RELATED LINKS</span></span>