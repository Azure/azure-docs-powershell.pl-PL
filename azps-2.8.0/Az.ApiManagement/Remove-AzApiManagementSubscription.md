---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 5d3ad3481a57f2578678daa88c1f3e87e9893f7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706931"
---
# <span data-ttu-id="87515-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="87515-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="87515-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87515-102">SYNOPSIS</span></span>
<span data-ttu-id="87515-103">Usuwa istniejącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="87515-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="87515-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87515-104">SYNTAX</span></span>

### <span data-ttu-id="87515-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="87515-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87515-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="87515-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87515-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="87515-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87515-108">Opis</span><span class="sxs-lookup"><span data-stu-id="87515-108">DESCRIPTION</span></span>
<span data-ttu-id="87515-109">Polecenie cmdlet **Remove-AzApiManagementSubscription** Usuwa istniejącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="87515-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="87515-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87515-110">EXAMPLES</span></span>

### <span data-ttu-id="87515-111">Przykład 1: usuwanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="87515-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="87515-112">To polecenie usuwa istniejącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="87515-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="87515-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87515-113">PARAMETERS</span></span>

### <span data-ttu-id="87515-114">-Context</span><span class="sxs-lookup"><span data-stu-id="87515-114">-Context</span></span>
<span data-ttu-id="87515-115">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="87515-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87515-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87515-116">-DefaultProfile</span></span>
<span data-ttu-id="87515-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87515-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87515-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="87515-118">-InputObject</span></span>
<span data-ttu-id="87515-119">Wystąpienie PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="87515-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="87515-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="87515-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87515-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87515-121">-PassThru</span></span>
<span data-ttu-id="87515-122">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiodło, lub wartość $false w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="87515-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="87515-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87515-123">-ResourceId</span></span>
<span data-ttu-id="87515-124">ARM ResourceId abonamentu.</span><span class="sxs-lookup"><span data-stu-id="87515-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="87515-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="87515-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87515-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="87515-126">-SubscriptionId</span></span>
<span data-ttu-id="87515-127">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="87515-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="87515-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87515-128">-Confirm</span></span>
<span data-ttu-id="87515-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87515-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87515-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87515-130">-WhatIf</span></span>
<span data-ttu-id="87515-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87515-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87515-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87515-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87515-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87515-133">CommonParameters</span></span>
<span data-ttu-id="87515-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87515-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87515-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87515-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87515-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87515-136">INPUTS</span></span>

### <span data-ttu-id="87515-137">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="87515-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="87515-138">System. String</span><span class="sxs-lookup"><span data-stu-id="87515-138">System.String</span></span>

### <span data-ttu-id="87515-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87515-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="87515-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87515-140">OUTPUTS</span></span>

### <span data-ttu-id="87515-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87515-141">System.Boolean</span></span>

## <span data-ttu-id="87515-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87515-142">NOTES</span></span>

## <span data-ttu-id="87515-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87515-143">RELATED LINKS</span></span>

[<span data-ttu-id="87515-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="87515-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="87515-145">Nowe — AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="87515-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="87515-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="87515-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)

