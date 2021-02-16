---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178035"
---
# <span data-ttu-id="65e93-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65e93-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="65e93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65e93-102">SYNOPSIS</span></span>
<span data-ttu-id="65e93-103">Usuwa istniejącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="65e93-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="65e93-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="65e93-104">SYNTAX</span></span>

### <span data-ttu-id="65e93-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="65e93-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65e93-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="65e93-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65e93-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65e93-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65e93-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="65e93-108">DESCRIPTION</span></span>
<span data-ttu-id="65e93-109">Polecenie **cmdlet Remove-AzApiManagementSubscription** usuwa istniejącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="65e93-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="65e93-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="65e93-110">EXAMPLES</span></span>

### <span data-ttu-id="65e93-111">Przykład 1. Usuwanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="65e93-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="65e93-112">To polecenie usuwa istniejącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="65e93-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="65e93-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65e93-113">PARAMETERS</span></span>

### <span data-ttu-id="65e93-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="65e93-114">-Context</span></span>
<span data-ttu-id="65e93-115">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="65e93-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="65e93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e93-116">-DefaultProfile</span></span>
<span data-ttu-id="65e93-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="65e93-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65e93-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65e93-118">-InputObject</span></span>
<span data-ttu-id="65e93-119">Wystąpienie funkcji PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="65e93-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="65e93-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="65e93-120">This parameter is required.</span></span>

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

### <span data-ttu-id="65e93-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65e93-121">-PassThru</span></span>
<span data-ttu-id="65e93-122">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiedzie, lub wartość $false w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="65e93-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="65e93-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65e93-123">-ResourceId</span></span>
<span data-ttu-id="65e93-124">Arm ResourceId of Subscription.</span><span class="sxs-lookup"><span data-stu-id="65e93-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="65e93-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="65e93-125">This parameter is required.</span></span>

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

### <span data-ttu-id="65e93-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65e93-126">-SubscriptionId</span></span>
<span data-ttu-id="65e93-127">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="65e93-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="65e93-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65e93-128">-Confirm</span></span>
<span data-ttu-id="65e93-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="65e93-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65e93-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65e93-130">-WhatIf</span></span>
<span data-ttu-id="65e93-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65e93-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65e93-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="65e93-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65e93-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e93-133">CommonParameters</span></span>
<span data-ttu-id="65e93-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65e93-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e93-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65e93-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e93-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65e93-136">INPUTS</span></span>

### <span data-ttu-id="65e93-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="65e93-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="65e93-138">System.String</span><span class="sxs-lookup"><span data-stu-id="65e93-138">System.String</span></span>

### <span data-ttu-id="65e93-139">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="65e93-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="65e93-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65e93-140">OUTPUTS</span></span>

### <span data-ttu-id="65e93-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65e93-141">System.Boolean</span></span>

## <span data-ttu-id="65e93-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="65e93-142">NOTES</span></span>

## <span data-ttu-id="65e93-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65e93-143">RELATED LINKS</span></span>

[<span data-ttu-id="65e93-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65e93-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="65e93-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65e93-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="65e93-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65e93-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


