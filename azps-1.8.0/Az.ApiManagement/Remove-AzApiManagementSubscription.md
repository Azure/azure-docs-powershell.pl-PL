---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 411fa67d81b772c2e9dcd6b1690e8eac50de3ea0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869396"
---
# <span data-ttu-id="ab1af-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ab1af-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="ab1af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab1af-102">SYNOPSIS</span></span>
<span data-ttu-id="ab1af-103">Usuwa istniejącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="ab1af-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="ab1af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab1af-104">SYNTAX</span></span>

```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab1af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab1af-105">DESCRIPTION</span></span>
<span data-ttu-id="ab1af-106">Polecenie cmdlet **Remove-AzApiManagementSubscription** Usuwa istniejącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="ab1af-106">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="ab1af-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab1af-107">EXAMPLES</span></span>

### <span data-ttu-id="ab1af-108">Przykład 1: usuwanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ab1af-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="ab1af-109">To polecenie usuwa istniejącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="ab1af-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="ab1af-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab1af-110">PARAMETERS</span></span>

### <span data-ttu-id="ab1af-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ab1af-111">-Context</span></span>
<span data-ttu-id="ab1af-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ab1af-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ab1af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab1af-113">-DefaultProfile</span></span>
<span data-ttu-id="ab1af-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab1af-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab1af-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab1af-115">-PassThru</span></span>
<span data-ttu-id="ab1af-116">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiodło, lub wartość $false w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="ab1af-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="ab1af-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ab1af-117">-SubscriptionId</span></span>
<span data-ttu-id="ab1af-118">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ab1af-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="ab1af-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab1af-119">-Confirm</span></span>
<span data-ttu-id="ab1af-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab1af-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab1af-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab1af-121">-WhatIf</span></span>
<span data-ttu-id="ab1af-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab1af-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab1af-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab1af-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab1af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab1af-124">CommonParameters</span></span>
<span data-ttu-id="ab1af-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab1af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab1af-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab1af-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab1af-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab1af-127">INPUTS</span></span>

### <span data-ttu-id="ab1af-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ab1af-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ab1af-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ab1af-129">System.String</span></span>

### <span data-ttu-id="ab1af-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ab1af-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ab1af-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab1af-131">OUTPUTS</span></span>

### <span data-ttu-id="ab1af-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab1af-132">System.Boolean</span></span>

## <span data-ttu-id="ab1af-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab1af-133">NOTES</span></span>

## <span data-ttu-id="ab1af-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab1af-134">RELATED LINKS</span></span>

[<span data-ttu-id="ab1af-135">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ab1af-135">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="ab1af-136">Nowe — AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ab1af-136">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="ab1af-137">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ab1af-137">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


