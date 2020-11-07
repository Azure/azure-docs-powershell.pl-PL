---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: 7cddd6ab52774c6ae377ecddb6883d5019d6d7fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719592"
---
# <span data-ttu-id="bc659-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bc659-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="bc659-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc659-102">SYNOPSIS</span></span>
<span data-ttu-id="bc659-103">Umożliwia pobieranie kont automatyzacji w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bc659-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc659-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc659-104">SYNTAX</span></span>

### <span data-ttu-id="bc659-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bc659-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc659-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bc659-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc659-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bc659-107">DESCRIPTION</span></span>
<span data-ttu-id="bc659-108">Polecenie cmdlet **Get-AzureRmAutomationAccount** pobiera konta usługi Azure Automation w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bc659-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>

<span data-ttu-id="bc659-109">Aby uzyskać więcej informacji na temat kont automatyzacji, zobacz polecenie cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="bc659-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="bc659-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc659-110">EXAMPLES</span></span>

### <span data-ttu-id="bc659-111">Przykład 1: pobieranie wszystkich kont</span><span class="sxs-lookup"><span data-stu-id="bc659-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="bc659-112">To polecenie umożliwia pobieranie wszystkich kont automatyzacji w grupie zasobów o nazwie ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="bc659-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="bc659-113">Przykład 2: Uzyskiwanie konta</span><span class="sxs-lookup"><span data-stu-id="bc659-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="bc659-114">To polecenie uzyskuje konto usługi Automation o nazwie ContosoAutomationAccount w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bc659-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="bc659-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc659-115">PARAMETERS</span></span>

### <span data-ttu-id="bc659-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc659-116">-DefaultProfile</span></span>
<span data-ttu-id="bc659-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bc659-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc659-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc659-118">-Name</span></span>
<span data-ttu-id="bc659-119">Określa nazwę konta automatyzacji, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc659-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc659-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc659-120">-ResourceGroupName</span></span>
<span data-ttu-id="bc659-121">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="bc659-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc659-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc659-122">CommonParameters</span></span>
<span data-ttu-id="bc659-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc659-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc659-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc659-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc659-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc659-125">INPUTS</span></span>

### <span data-ttu-id="bc659-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bc659-126">None</span></span>
<span data-ttu-id="bc659-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="bc659-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bc659-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc659-128">OUTPUTS</span></span>

### <span data-ttu-id="bc659-129">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bc659-129">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="bc659-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc659-130">NOTES</span></span>

## <span data-ttu-id="bc659-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc659-131">RELATED LINKS</span></span>

[<span data-ttu-id="bc659-132">Nowe — AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bc659-132">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="bc659-133">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bc659-133">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="bc659-134">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bc659-134">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


