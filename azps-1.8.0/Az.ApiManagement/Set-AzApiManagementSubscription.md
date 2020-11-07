---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: cbdc876368f55ace6f77c04172dc2f0a53b0a7f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710632"
---
# <span data-ttu-id="1f294-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1f294-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="1f294-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f294-102">SYNOPSIS</span></span>
<span data-ttu-id="1f294-103">Umożliwia ustawienie istniejących szczegółów subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f294-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="1f294-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f294-104">SYNTAX</span></span>

```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Name <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f294-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f294-105">DESCRIPTION</span></span>
<span data-ttu-id="1f294-106">Polecenie cmdlet **Set-AzApiManagementSubscription** ustawia istniejące dane subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f294-106">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="1f294-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f294-107">EXAMPLES</span></span>

### <span data-ttu-id="1f294-108">Przykład 1: Ustawianie kluczy stanów i podstawowych i pomocniczych dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1f294-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="1f294-109">To polecenie ustawia podstawowe i pomocnicze klucze subskrypcji oraz uaktywnia je.</span><span class="sxs-lookup"><span data-stu-id="1f294-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="1f294-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f294-110">PARAMETERS</span></span>

### <span data-ttu-id="1f294-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1f294-111">-Context</span></span>
<span data-ttu-id="1f294-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1f294-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1f294-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f294-113">-DefaultProfile</span></span>
<span data-ttu-id="1f294-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f294-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f294-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="1f294-115">-ExpiresOn</span></span>
<span data-ttu-id="1f294-116">Określa datę wygaśnięcia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f294-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="1f294-117">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="1f294-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="1f294-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f294-118">-Name</span></span>
<span data-ttu-id="1f294-119">Określa nazwę subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f294-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="1f294-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f294-120">-PassThru</span></span>
<span data-ttu-id="1f294-121">passthru</span><span class="sxs-lookup"><span data-stu-id="1f294-121">passthru</span></span>

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

### <span data-ttu-id="1f294-122">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="1f294-122">-PrimaryKey</span></span>
<span data-ttu-id="1f294-123">Określa klucz podstawowy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f294-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="1f294-124">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="1f294-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="1f294-125">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="1f294-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="1f294-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="1f294-126">-SecondaryKey</span></span>
<span data-ttu-id="1f294-127">Określa klucz pomocniczy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f294-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="1f294-128">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="1f294-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="1f294-129">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="1f294-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="1f294-130">-State</span><span class="sxs-lookup"><span data-stu-id="1f294-130">-State</span></span>
<span data-ttu-id="1f294-131">Określa stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="1f294-131">Specifies the subscription state.</span></span>
<span data-ttu-id="1f294-132">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="1f294-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="1f294-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="1f294-133">-StateComment</span></span>
<span data-ttu-id="1f294-134">Umożliwia określenie komentarza dotyczącego stanu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f294-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="1f294-135">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="1f294-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="1f294-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1f294-136">-SubscriptionId</span></span>
<span data-ttu-id="1f294-137">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f294-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="1f294-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f294-138">CommonParameters</span></span>
<span data-ttu-id="1f294-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f294-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f294-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f294-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f294-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f294-141">INPUTS</span></span>

### <span data-ttu-id="1f294-142">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1f294-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1f294-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1f294-143">System.String</span></span>

### <span data-ttu-id="1f294-144">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1f294-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1f294-145">System. Nullable "1 [[System. DateTime, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1f294-145">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1f294-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1f294-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1f294-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f294-147">OUTPUTS</span></span>

### <span data-ttu-id="1f294-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1f294-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="1f294-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f294-149">NOTES</span></span>

## <span data-ttu-id="1f294-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f294-150">RELATED LINKS</span></span>

[<span data-ttu-id="1f294-151">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1f294-151">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="1f294-152">Nowe — AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1f294-152">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="1f294-153">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1f294-153">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


