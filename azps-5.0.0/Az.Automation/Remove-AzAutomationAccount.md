---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307489"
---
# <span data-ttu-id="7165b-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7165b-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="7165b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7165b-102">SYNOPSIS</span></span>
<span data-ttu-id="7165b-103">Usuwa konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="7165b-103">Removes an Automation account.</span></span>

## <span data-ttu-id="7165b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7165b-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7165b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7165b-105">DESCRIPTION</span></span>
<span data-ttu-id="7165b-106">Polecenie cmdlet **Remove-AzAutomationAccount** usuwa konto usługi Azure Automation z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7165b-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="7165b-107">Aby uzyskać więcej informacji na temat kont automatyzacji, zobacz polecenie cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="7165b-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="7165b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7165b-108">EXAMPLES</span></span>

### <span data-ttu-id="7165b-109">Przykład 1: usuwanie konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="7165b-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7165b-110">To polecenie usuwa konto usługi Automation o nazwie ContosoAutomationAccount bez monitowania o weryfikację użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7165b-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="7165b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7165b-111">PARAMETERS</span></span>

### <span data-ttu-id="7165b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7165b-112">-DefaultProfile</span></span>
<span data-ttu-id="7165b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7165b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7165b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="7165b-114">-Force</span></span>
<span data-ttu-id="7165b-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="7165b-115">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7165b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7165b-116">-Name</span></span>
<span data-ttu-id="7165b-117">Określa nazwę konta automatyzacji, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7165b-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7165b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7165b-118">-ResourceGroupName</span></span>
<span data-ttu-id="7165b-119">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="7165b-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="7165b-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7165b-120">-Confirm</span></span>
<span data-ttu-id="7165b-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7165b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7165b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7165b-122">-WhatIf</span></span>
<span data-ttu-id="7165b-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7165b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7165b-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7165b-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7165b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7165b-125">CommonParameters</span></span>
<span data-ttu-id="7165b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7165b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7165b-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7165b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7165b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7165b-128">INPUTS</span></span>

### <span data-ttu-id="7165b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7165b-129">System.String</span></span>

## <span data-ttu-id="7165b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7165b-130">OUTPUTS</span></span>

### <span data-ttu-id="7165b-131">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7165b-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="7165b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7165b-132">NOTES</span></span>

## <span data-ttu-id="7165b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7165b-133">RELATED LINKS</span></span>

[<span data-ttu-id="7165b-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7165b-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="7165b-135">Nowe — AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7165b-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="7165b-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7165b-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


