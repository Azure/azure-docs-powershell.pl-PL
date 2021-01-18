---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 2f5aef61ad89bc7ac4879c3a40880522a52020e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502287"
---
# <span data-ttu-id="f5f0f-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f5f0f-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="f5f0f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f0f-103">Usuwa poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f5f0f-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="f5f0f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5f0f-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5f0f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f5f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f0f-106">Polecenie cmdlet **Remove-AzAutomationCredential** usuwa poświadczenia z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f5f0f-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="f5f0f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5f0f-107">EXAMPLES</span></span>

### <span data-ttu-id="f5f0f-108">Przykład 1: usuwanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="f5f0f-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f5f0f-109">To polecenie usuwa poświadczenia o nazwie ContosoCredential na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f5f0f-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f5f0f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5f0f-110">PARAMETERS</span></span>

### <span data-ttu-id="f5f0f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f5f0f-111">-AutomationAccountName</span></span>
<span data-ttu-id="f5f0f-112">Określa nazwę konta automatyzacji, na podstawie którego to polecenie cmdlet usuwa poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="f5f0f-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="f5f0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f0f-113">-DefaultProfile</span></span>
<span data-ttu-id="f5f0f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f5f0f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5f0f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5f0f-115">-Name</span></span>
<span data-ttu-id="f5f0f-116">Określa nazwę poświadczenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5f0f-116">Specifies the name of the credential that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f0f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f0f-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5f0f-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet usunie poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="f5f0f-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="f5f0f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5f0f-119">-Confirm</span></span>
<span data-ttu-id="f5f0f-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5f0f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5f0f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5f0f-121">-WhatIf</span></span>
<span data-ttu-id="f5f0f-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5f0f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5f0f-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f5f0f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5f0f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f0f-124">CommonParameters</span></span>
<span data-ttu-id="f5f0f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f0f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f0f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f0f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f0f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5f0f-127">INPUTS</span></span>

### <span data-ttu-id="f5f0f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f5f0f-128">System.String</span></span>

## <span data-ttu-id="f5f0f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5f0f-129">OUTPUTS</span></span>

### <span data-ttu-id="f5f0f-130">System. void</span><span class="sxs-lookup"><span data-stu-id="f5f0f-130">System.Void</span></span>

## <span data-ttu-id="f5f0f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5f0f-131">NOTES</span></span>

## <span data-ttu-id="f5f0f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5f0f-132">RELATED LINKS</span></span>

[<span data-ttu-id="f5f0f-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f5f0f-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="f5f0f-134">Nowe — AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f5f0f-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="f5f0f-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f5f0f-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


