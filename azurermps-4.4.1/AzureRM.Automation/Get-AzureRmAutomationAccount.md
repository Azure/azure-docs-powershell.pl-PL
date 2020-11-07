---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: d79f46e645bb5889c58aaca4b3fbdd046be5c756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717879"
---
# <span data-ttu-id="77f27-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="77f27-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="77f27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77f27-102">SYNOPSIS</span></span>
<span data-ttu-id="77f27-103">Umożliwia pobieranie kont automatyzacji w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="77f27-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77f27-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77f27-104">SYNTAX</span></span>

### <span data-ttu-id="77f27-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77f27-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77f27-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="77f27-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77f27-107">Opis</span><span class="sxs-lookup"><span data-stu-id="77f27-107">DESCRIPTION</span></span>
<span data-ttu-id="77f27-108">Polecenie cmdlet **Get-AzureRmAutomationAccount** pobiera konta usługi Azure Automation w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="77f27-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>

<span data-ttu-id="77f27-109">Aby uzyskać więcej informacji na temat kont automatyzacji, zobacz polecenie cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="77f27-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="77f27-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77f27-110">EXAMPLES</span></span>

### <span data-ttu-id="77f27-111">Przykład 1: pobieranie wszystkich kont</span><span class="sxs-lookup"><span data-stu-id="77f27-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="77f27-112">To polecenie umożliwia pobieranie wszystkich kont automatyzacji w grupie zasobów o nazwie ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="77f27-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="77f27-113">Przykład 2: Uzyskiwanie konta</span><span class="sxs-lookup"><span data-stu-id="77f27-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="77f27-114">To polecenie uzyskuje konto usługi Automation o nazwie ContosoAutomationAccount w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="77f27-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="77f27-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77f27-115">PARAMETERS</span></span>

### <span data-ttu-id="77f27-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77f27-116">-Name</span></span>
<span data-ttu-id="77f27-117">Określa nazwę konta automatyzacji, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77f27-117">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f27-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f27-118">-ResourceGroupName</span></span>
<span data-ttu-id="77f27-119">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="77f27-119">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f27-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f27-120">-DefaultProfile</span></span>
<span data-ttu-id="77f27-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77f27-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77f27-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f27-122">CommonParameters</span></span>
<span data-ttu-id="77f27-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f27-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f27-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77f27-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f27-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77f27-125">INPUTS</span></span>

## <span data-ttu-id="77f27-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77f27-126">OUTPUTS</span></span>

### <span data-ttu-id="77f27-127">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="77f27-127">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="77f27-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77f27-128">NOTES</span></span>

## <span data-ttu-id="77f27-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77f27-129">RELATED LINKS</span></span>

[<span data-ttu-id="77f27-130">Nowe — AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="77f27-130">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="77f27-131">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="77f27-131">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="77f27-132">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="77f27-132">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


