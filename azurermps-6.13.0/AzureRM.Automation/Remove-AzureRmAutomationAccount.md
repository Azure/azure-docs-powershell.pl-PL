---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: e3dd0d475a2a2c34dfa7912bf9ced4ef958295c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542008"
---
# <span data-ttu-id="f4c91-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f4c91-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="f4c91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4c91-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c91-103">Usuwa konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="f4c91-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4c91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4c91-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4c91-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f4c91-105">DESCRIPTION</span></span>
<span data-ttu-id="f4c91-106">Polecenie cmdlet **Remove-AzureRmAutomationAccount** usuwa konto usługi Azure Automation z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4c91-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="f4c91-107">Aby uzyskać więcej informacji na temat kont automatyzacji, zobacz polecenie cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="f4c91-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="f4c91-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4c91-108">EXAMPLES</span></span>

### <span data-ttu-id="f4c91-109">Przykład 1: usuwanie konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="f4c91-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f4c91-110">To polecenie usuwa konto usługi Automation o nazwie ContosoAutomationAccount bez monitowania o weryfikację użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f4c91-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="f4c91-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4c91-111">PARAMETERS</span></span>

### <span data-ttu-id="f4c91-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c91-112">-DefaultProfile</span></span>
<span data-ttu-id="f4c91-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f4c91-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4c91-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f4c91-114">-Force</span></span>
<span data-ttu-id="f4c91-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="f4c91-115">ps_force</span></span>

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

### <span data-ttu-id="f4c91-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f4c91-116">-Name</span></span>
<span data-ttu-id="f4c91-117">Określa nazwę konta automatyzacji, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4c91-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f4c91-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4c91-118">-ResourceGroupName</span></span>
<span data-ttu-id="f4c91-119">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="f4c91-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="f4c91-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f4c91-120">-Confirm</span></span>
<span data-ttu-id="f4c91-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4c91-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4c91-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c91-122">-WhatIf</span></span>
<span data-ttu-id="f4c91-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4c91-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4c91-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f4c91-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4c91-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c91-125">CommonParameters</span></span>
<span data-ttu-id="f4c91-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4c91-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c91-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4c91-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c91-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4c91-128">INPUTS</span></span>

### <span data-ttu-id="f4c91-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f4c91-129">System.String</span></span>

## <span data-ttu-id="f4c91-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4c91-130">OUTPUTS</span></span>

### <span data-ttu-id="f4c91-131">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f4c91-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="f4c91-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4c91-132">NOTES</span></span>

## <span data-ttu-id="f4c91-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4c91-133">RELATED LINKS</span></span>

[<span data-ttu-id="f4c91-134">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f4c91-134">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="f4c91-135">Nowe — AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f4c91-135">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="f4c91-136">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f4c91-136">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


