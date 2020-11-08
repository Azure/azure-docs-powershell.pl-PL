---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053135"
---
# <span data-ttu-id="a00bb-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a00bb-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="a00bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a00bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a00bb-103">Umożliwia ustawienie istniejących szczegółów subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a00bb-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="a00bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a00bb-104">SYNTAX</span></span>

### <span data-ttu-id="a00bb-105">ByInputObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a00bb-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a00bb-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="a00bb-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a00bb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a00bb-107">DESCRIPTION</span></span>
<span data-ttu-id="a00bb-108">Polecenie cmdlet **Set-AzApiManagementSubscription** ustawia istniejące dane subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a00bb-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="a00bb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a00bb-109">EXAMPLES</span></span>

### <span data-ttu-id="a00bb-110">Przykład 1: Ustawianie kluczy stanów i podstawowych i pomocniczych dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a00bb-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="a00bb-111">To polecenie ustawia podstawowe i pomocnicze klucze subskrypcji oraz uaktywnia je.</span><span class="sxs-lookup"><span data-stu-id="a00bb-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="a00bb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a00bb-112">PARAMETERS</span></span>

### <span data-ttu-id="a00bb-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a00bb-113">-Context</span></span>
<span data-ttu-id="a00bb-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a00bb-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a00bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a00bb-115">-DefaultProfile</span></span>
<span data-ttu-id="a00bb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a00bb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a00bb-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="a00bb-117">-ExpiresOn</span></span>
<span data-ttu-id="a00bb-118">Określa datę wygaśnięcia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a00bb-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="a00bb-119">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="a00bb-119">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00bb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a00bb-120">-InputObject</span></span>
<span data-ttu-id="a00bb-121">Wystąpienie PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="a00bb-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="a00bb-122">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a00bb-122">This parameter is required.</span></span>

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

### <span data-ttu-id="a00bb-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a00bb-123">-Name</span></span>
<span data-ttu-id="a00bb-124">Określa nazwę subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a00bb-124">Specifies a subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00bb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a00bb-125">-PassThru</span></span>
<span data-ttu-id="a00bb-126">passthru</span><span class="sxs-lookup"><span data-stu-id="a00bb-126">passthru</span></span>

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

### <span data-ttu-id="a00bb-127">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="a00bb-127">-PrimaryKey</span></span>
<span data-ttu-id="a00bb-128">Określa klucz podstawowy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a00bb-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="a00bb-129">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="a00bb-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="a00bb-130">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="a00bb-130">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00bb-131">-Zakres</span><span class="sxs-lookup"><span data-stu-id="a00bb-131">-Scope</span></span>
<span data-ttu-id="a00bb-132">Zakres subskrypcji, niezależnie od tego, czy jest to zakres API/apis/{apiId}, czy zakres/products/{productId} lub globalny zakres interfejsu API/Apis czy globalny zakres/.</span><span class="sxs-lookup"><span data-stu-id="a00bb-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="a00bb-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a00bb-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00bb-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="a00bb-134">-SecondaryKey</span></span>
<span data-ttu-id="a00bb-135">Określa klucz pomocniczy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a00bb-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="a00bb-136">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="a00bb-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="a00bb-137">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="a00bb-137">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00bb-138">-State</span><span class="sxs-lookup"><span data-stu-id="a00bb-138">-State</span></span>
<span data-ttu-id="a00bb-139">Określa stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a00bb-139">Specifies the subscription state.</span></span>
<span data-ttu-id="a00bb-140">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="a00bb-140">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00bb-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="a00bb-141">-StateComment</span></span>
<span data-ttu-id="a00bb-142">Umożliwia określenie komentarza dotyczącego stanu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a00bb-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="a00bb-143">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="a00bb-143">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00bb-144">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a00bb-144">-SubscriptionId</span></span>
<span data-ttu-id="a00bb-145">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a00bb-145">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00bb-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="a00bb-146">-UserId</span></span>
<span data-ttu-id="a00bb-147">Właściciel subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a00bb-147">The owner of the subscription.</span></span> <span data-ttu-id="a00bb-148">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a00bb-148">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00bb-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a00bb-149">-Confirm</span></span>
<span data-ttu-id="a00bb-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a00bb-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00bb-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a00bb-151">-WhatIf</span></span>
<span data-ttu-id="a00bb-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a00bb-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a00bb-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a00bb-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00bb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a00bb-154">CommonParameters</span></span>
<span data-ttu-id="a00bb-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a00bb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a00bb-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a00bb-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a00bb-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a00bb-157">INPUTS</span></span>

### <span data-ttu-id="a00bb-158">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a00bb-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a00bb-159">System. String</span><span class="sxs-lookup"><span data-stu-id="a00bb-159">System.String</span></span>

### <span data-ttu-id="a00bb-160">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a00bb-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a00bb-161">System. Nullable "1 [[System. DateTime, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a00bb-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a00bb-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a00bb-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a00bb-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a00bb-163">OUTPUTS</span></span>

### <span data-ttu-id="a00bb-164">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a00bb-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="a00bb-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a00bb-165">NOTES</span></span>

## <span data-ttu-id="a00bb-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a00bb-166">RELATED LINKS</span></span>

[<span data-ttu-id="a00bb-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a00bb-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="a00bb-168">Nowe — AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a00bb-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="a00bb-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a00bb-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


