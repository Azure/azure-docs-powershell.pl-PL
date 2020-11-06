---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 2c98cde73610a7a72b237bbe268f527fefaf71a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548391"
---
# <span data-ttu-id="6e679-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6e679-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="6e679-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e679-102">SYNOPSIS</span></span>
<span data-ttu-id="6e679-103">Usuwa poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="6e679-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e679-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e679-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e679-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6e679-105">DESCRIPTION</span></span>
<span data-ttu-id="6e679-106">Polecenie cmdlet **Remove-AzureRmAutomationCredential** usuwa poświadczenia z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6e679-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="6e679-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e679-107">EXAMPLES</span></span>

### <span data-ttu-id="6e679-108">Przykład 1: usuwanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="6e679-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6e679-109">To polecenie usuwa poświadczenia o nazwie ContosoCredential na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6e679-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="6e679-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e679-110">PARAMETERS</span></span>

### <span data-ttu-id="6e679-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6e679-111">-AutomationAccountName</span></span>
<span data-ttu-id="6e679-112">Określa nazwę konta automatyzacji, na podstawie którego to polecenie cmdlet usuwa poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="6e679-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="6e679-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e679-113">-Name</span></span>
<span data-ttu-id="6e679-114">Określa nazwę poświadczenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e679-114">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6e679-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e679-115">-ResourceGroupName</span></span>
<span data-ttu-id="6e679-116">Określa nazwę grupy zasobów, dla której to polecenie cmdlet usunie poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="6e679-116">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="6e679-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e679-117">-Confirm</span></span>
<span data-ttu-id="6e679-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e679-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e679-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e679-119">-WhatIf</span></span>
<span data-ttu-id="6e679-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e679-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e679-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e679-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e679-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e679-122">-DefaultProfile</span></span>
<span data-ttu-id="6e679-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e679-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e679-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e679-124">CommonParameters</span></span>
<span data-ttu-id="6e679-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e679-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e679-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e679-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e679-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e679-127">INPUTS</span></span>

## <span data-ttu-id="6e679-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e679-128">OUTPUTS</span></span>

## <span data-ttu-id="6e679-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e679-129">NOTES</span></span>

## <span data-ttu-id="6e679-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e679-130">RELATED LINKS</span></span>

[<span data-ttu-id="6e679-131">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6e679-131">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="6e679-132">Nowe — AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6e679-132">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="6e679-133">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6e679-133">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


