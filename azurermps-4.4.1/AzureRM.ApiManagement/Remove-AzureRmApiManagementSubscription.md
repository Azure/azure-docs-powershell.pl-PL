---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: fd232a0f118db5730c41ef1588eaf07d80df69f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525754"
---
# <span data-ttu-id="1893a-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1893a-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="1893a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1893a-102">SYNOPSIS</span></span>
<span data-ttu-id="1893a-103">Usuwa istniejącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="1893a-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1893a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1893a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1893a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1893a-105">DESCRIPTION</span></span>
<span data-ttu-id="1893a-106">Polecenie cmdlet **Remove-AzureRmApiManagementSubscription** Usuwa istniejącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="1893a-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="1893a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1893a-107">EXAMPLES</span></span>

### <span data-ttu-id="1893a-108">Przykład 1: usuwanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1893a-108">Example 1: Delete a subscription</span></span>
```
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="1893a-109">To polecenie usuwa istniejącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="1893a-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="1893a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1893a-110">PARAMETERS</span></span>

### <span data-ttu-id="1893a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1893a-111">-Context</span></span>
<span data-ttu-id="1893a-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1893a-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1893a-113">-PassThru</span></span>
<span data-ttu-id="1893a-114">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiodło, lub wartość $false w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="1893a-114">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1893a-115">-SubscriptionId</span></span>
<span data-ttu-id="1893a-116">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1893a-116">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1893a-117">-Confirm</span></span>
<span data-ttu-id="1893a-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1893a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1893a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1893a-119">-WhatIf</span></span>
<span data-ttu-id="1893a-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1893a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1893a-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1893a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1893a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1893a-122">-DefaultProfile</span></span>
<span data-ttu-id="1893a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1893a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1893a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1893a-124">CommonParameters</span></span>
<span data-ttu-id="1893a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1893a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1893a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1893a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1893a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1893a-127">INPUTS</span></span>

## <span data-ttu-id="1893a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1893a-128">OUTPUTS</span></span>

### <span data-ttu-id="1893a-129">Wartość</span><span class="sxs-lookup"><span data-stu-id="1893a-129">Boolean</span></span>

## <span data-ttu-id="1893a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1893a-130">NOTES</span></span>

## <span data-ttu-id="1893a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1893a-131">RELATED LINKS</span></span>

[<span data-ttu-id="1893a-132">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1893a-132">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="1893a-133">Nowe — AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1893a-133">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="1893a-134">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1893a-134">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


