---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 6c5e0a376b8170c73abc394f275995b178e90917
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710609"
---
# <span data-ttu-id="f4d78-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f4d78-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="f4d78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4d78-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d78-103">Umożliwia pobieranie kont automatyzacji w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4d78-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="f4d78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4d78-104">SYNTAX</span></span>

### <span data-ttu-id="f4d78-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f4d78-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4d78-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f4d78-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4d78-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f4d78-107">DESCRIPTION</span></span>
<span data-ttu-id="f4d78-108">Polecenie cmdlet **Get-AzAutomationAccount** pobiera konta usługi Azure Automation w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4d78-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="f4d78-109">Aby uzyskać więcej informacji na temat kont automatyzacji, zobacz polecenie cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="f4d78-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="f4d78-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4d78-110">EXAMPLES</span></span>

### <span data-ttu-id="f4d78-111">Przykład 1: pobieranie wszystkich kont</span><span class="sxs-lookup"><span data-stu-id="f4d78-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="f4d78-112">To polecenie umożliwia pobieranie wszystkich kont automatyzacji w grupie zasobów o nazwie ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="f4d78-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="f4d78-113">Przykład 2: Uzyskiwanie konta</span><span class="sxs-lookup"><span data-stu-id="f4d78-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="f4d78-114">To polecenie uzyskuje konto usługi Automation o nazwie ContosoAutomationAccount w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f4d78-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="f4d78-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4d78-115">PARAMETERS</span></span>

### <span data-ttu-id="f4d78-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d78-116">-DefaultProfile</span></span>
<span data-ttu-id="f4d78-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f4d78-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4d78-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f4d78-118">-Name</span></span>
<span data-ttu-id="f4d78-119">Określa nazwę konta automatyzacji, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4d78-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f4d78-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d78-120">-ResourceGroupName</span></span>
<span data-ttu-id="f4d78-121">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f4d78-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="f4d78-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d78-122">CommonParameters</span></span>
<span data-ttu-id="f4d78-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d78-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d78-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d78-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d78-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4d78-125">INPUTS</span></span>

### <span data-ttu-id="f4d78-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f4d78-126">System.String</span></span>

## <span data-ttu-id="f4d78-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4d78-127">OUTPUTS</span></span>

### <span data-ttu-id="f4d78-128">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f4d78-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="f4d78-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4d78-129">NOTES</span></span>

## <span data-ttu-id="f4d78-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4d78-130">RELATED LINKS</span></span>

[<span data-ttu-id="f4d78-131">Nowe — AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f4d78-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="f4d78-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f4d78-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="f4d78-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f4d78-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


