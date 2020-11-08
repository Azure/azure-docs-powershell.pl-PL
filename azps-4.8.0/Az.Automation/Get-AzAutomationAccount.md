---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063692"
---
# <span data-ttu-id="9e794-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9e794-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="9e794-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e794-102">SYNOPSIS</span></span>
<span data-ttu-id="9e794-103">Umożliwia pobieranie kont automatyzacji w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e794-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="9e794-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e794-104">SYNTAX</span></span>

### <span data-ttu-id="9e794-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9e794-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e794-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e794-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e794-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9e794-107">DESCRIPTION</span></span>
<span data-ttu-id="9e794-108">Polecenie cmdlet **Get-AzAutomationAccount** pobiera konta usługi Azure Automation w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e794-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="9e794-109">Aby uzyskać więcej informacji na temat kont automatyzacji, zobacz polecenie cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="9e794-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="9e794-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e794-110">EXAMPLES</span></span>

### <span data-ttu-id="9e794-111">Przykład 1: pobieranie wszystkich kont</span><span class="sxs-lookup"><span data-stu-id="9e794-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="9e794-112">To polecenie umożliwia pobieranie wszystkich kont automatyzacji w grupie zasobów o nazwie ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="9e794-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="9e794-113">Przykład 2: Uzyskiwanie konta</span><span class="sxs-lookup"><span data-stu-id="9e794-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="9e794-114">To polecenie uzyskuje konto usługi Automation o nazwie ContosoAutomationAccount w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9e794-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="9e794-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e794-115">PARAMETERS</span></span>

### <span data-ttu-id="9e794-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e794-116">-DefaultProfile</span></span>
<span data-ttu-id="9e794-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9e794-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e794-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e794-118">-Name</span></span>
<span data-ttu-id="9e794-119">Określa nazwę konta automatyzacji, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e794-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9e794-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e794-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e794-121">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9e794-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="9e794-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e794-122">CommonParameters</span></span>
<span data-ttu-id="9e794-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e794-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e794-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e794-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e794-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e794-125">INPUTS</span></span>

### <span data-ttu-id="9e794-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9e794-126">System.String</span></span>

## <span data-ttu-id="9e794-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e794-127">OUTPUTS</span></span>

### <span data-ttu-id="9e794-128">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9e794-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="9e794-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e794-129">NOTES</span></span>

## <span data-ttu-id="9e794-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e794-130">RELATED LINKS</span></span>

[<span data-ttu-id="9e794-131">Nowe — AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9e794-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="9e794-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9e794-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="9e794-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9e794-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


