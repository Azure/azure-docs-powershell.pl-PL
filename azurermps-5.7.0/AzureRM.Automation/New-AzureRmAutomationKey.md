---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 0f8cbf67af4cc62c5cdeaae216a2c0a63cbe5afc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553695"
---
# <span data-ttu-id="a0ca3-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="a0ca3-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="a0ca3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ca3-103">Regeneruje klucze rejestracji dla konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a0ca3-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0ca3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0ca3-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0ca3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a0ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="a0ca3-106">Polecenie cmdlet **New-AzureRmAutomationKey** generuje klucze rejestracji dla konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a0ca3-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="a0ca3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0ca3-107">EXAMPLES</span></span>

### <span data-ttu-id="a0ca3-108">Przykład 1. Regeneruj klucz dla konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="a0ca3-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="a0ca3-109">To polecenie generuje klucz podstawowy dla konta usługi Azure Automation o nazwie AutomationAccount01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a0ca3-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a0ca3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0ca3-110">PARAMETERS</span></span>

### <span data-ttu-id="a0ca3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a0ca3-111">-AutomationAccountName</span></span>
<span data-ttu-id="a0ca3-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet ponownie generuje klucze.</span><span class="sxs-lookup"><span data-stu-id="a0ca3-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ca3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ca3-113">-DefaultProfile</span></span>
<span data-ttu-id="a0ca3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a0ca3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ca3-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="a0ca3-115">-KeyType</span></span>
<span data-ttu-id="a0ca3-116">Określa typ klucza rejestracji agenta.</span><span class="sxs-lookup"><span data-stu-id="a0ca3-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="a0ca3-117">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="a0ca3-117">Valid values are:</span></span> 

- <span data-ttu-id="a0ca3-118">Początkowe</span><span class="sxs-lookup"><span data-stu-id="a0ca3-118">Primary</span></span> 
- <span data-ttu-id="a0ca3-119">Dodatkowej</span><span class="sxs-lookup"><span data-stu-id="a0ca3-119">Secondary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ca3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ca3-120">-ResourceGroupName</span></span>
<span data-ttu-id="a0ca3-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0ca3-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a0ca3-122">To polecenie cmdlet ponownie generuje klucze dla konta automatyzacji w grupie zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="a0ca3-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ca3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ca3-123">CommonParameters</span></span>
<span data-ttu-id="a0ca3-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0ca3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ca3-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0ca3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ca3-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0ca3-126">INPUTS</span></span>

### <span data-ttu-id="a0ca3-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a0ca3-127">None</span></span>
<span data-ttu-id="a0ca3-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a0ca3-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0ca3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0ca3-129">OUTPUTS</span></span>

### <span data-ttu-id="a0ca3-130">Microsoft. Azure. Commands. Automation. model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="a0ca3-130">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="a0ca3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0ca3-131">NOTES</span></span>

## <span data-ttu-id="a0ca3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0ca3-132">RELATED LINKS</span></span>

