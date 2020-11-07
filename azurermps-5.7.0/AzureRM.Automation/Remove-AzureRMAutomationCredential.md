---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 11b6772325c3e5170c697b21d25092fd96f3e2e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719195"
---
# <span data-ttu-id="4c3e1-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4c3e1-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="4c3e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c3e1-102">SYNOPSIS</span></span>
<span data-ttu-id="4c3e1-103">Usuwa poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4c3e1-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c3e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c3e1-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c3e1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c3e1-105">DESCRIPTION</span></span>
<span data-ttu-id="4c3e1-106">Polecenie cmdlet **Remove-AzureRmAutomationCredential** usuwa poświadczenia z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4c3e1-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="4c3e1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c3e1-107">EXAMPLES</span></span>

### <span data-ttu-id="4c3e1-108">Przykład 1: usuwanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="4c3e1-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4c3e1-109">To polecenie usuwa poświadczenia o nazwie ContosoCredential na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4c3e1-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="4c3e1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c3e1-110">PARAMETERS</span></span>

### <span data-ttu-id="4c3e1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4c3e1-111">-AutomationAccountName</span></span>
<span data-ttu-id="4c3e1-112">Określa nazwę konta automatyzacji, na podstawie którego to polecenie cmdlet usuwa poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="4c3e1-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="4c3e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c3e1-113">-DefaultProfile</span></span>
<span data-ttu-id="4c3e1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4c3e1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c3e1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c3e1-115">-Name</span></span>
<span data-ttu-id="4c3e1-116">Określa nazwę poświadczenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c3e1-116">Specifies the name of the credential that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c3e1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c3e1-117">-ResourceGroupName</span></span>
<span data-ttu-id="4c3e1-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet usunie poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="4c3e1-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="4c3e1-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c3e1-119">-Confirm</span></span>
<span data-ttu-id="4c3e1-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c3e1-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c3e1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c3e1-121">-WhatIf</span></span>
<span data-ttu-id="4c3e1-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c3e1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c3e1-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4c3e1-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c3e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c3e1-124">CommonParameters</span></span>
<span data-ttu-id="4c3e1-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c3e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c3e1-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c3e1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c3e1-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c3e1-127">INPUTS</span></span>

### <span data-ttu-id="4c3e1-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4c3e1-128">None</span></span>
<span data-ttu-id="4c3e1-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4c3e1-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c3e1-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c3e1-130">OUTPUTS</span></span>

## <span data-ttu-id="4c3e1-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c3e1-131">NOTES</span></span>

## <span data-ttu-id="4c3e1-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c3e1-132">RELATED LINKS</span></span>

[<span data-ttu-id="4c3e1-133">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4c3e1-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="4c3e1-134">Nowe — AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4c3e1-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="4c3e1-135">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4c3e1-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


