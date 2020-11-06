---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: c747d85f87e88c3f72ae86c8bcef771b3e42c91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526373"
---
# <span data-ttu-id="196be-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="196be-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="196be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="196be-102">SYNOPSIS</span></span>
<span data-ttu-id="196be-103">Umożliwia ustawienie istniejących szczegółów subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="196be-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="196be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="196be-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="196be-105">Opis</span><span class="sxs-lookup"><span data-stu-id="196be-105">DESCRIPTION</span></span>
<span data-ttu-id="196be-106">Polecenie cmdlet **Set-AzureRmApiManagementSubscription** ustawia istniejące dane subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="196be-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="196be-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="196be-107">EXAMPLES</span></span>

### <span data-ttu-id="196be-108">Przykład 1: Ustawianie kluczy stanów i podstawowych i pomocniczych dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="196be-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="196be-109">To polecenie ustawia podstawowe i pomocnicze klucze subskrypcji oraz uaktywnia je.</span><span class="sxs-lookup"><span data-stu-id="196be-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="196be-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="196be-110">PARAMETERS</span></span>

### <span data-ttu-id="196be-111">-Context</span><span class="sxs-lookup"><span data-stu-id="196be-111">-Context</span></span>
<span data-ttu-id="196be-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="196be-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="196be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196be-113">-DefaultProfile</span></span>
<span data-ttu-id="196be-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="196be-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="196be-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="196be-115">-ExpiresOn</span></span>
<span data-ttu-id="196be-116">Określa datę wygaśnięcia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="196be-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="196be-117">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="196be-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="196be-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="196be-118">-Name</span></span>
<span data-ttu-id="196be-119">Określa nazwę subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="196be-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="196be-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="196be-120">-PassThru</span></span>
<span data-ttu-id="196be-121">passthru</span><span class="sxs-lookup"><span data-stu-id="196be-121">passthru</span></span>

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

### <span data-ttu-id="196be-122">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="196be-122">-PrimaryKey</span></span>
<span data-ttu-id="196be-123">Określa klucz podstawowy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="196be-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="196be-124">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="196be-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="196be-125">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="196be-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="196be-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="196be-126">-SecondaryKey</span></span>
<span data-ttu-id="196be-127">Określa klucz pomocniczy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="196be-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="196be-128">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="196be-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="196be-129">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="196be-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="196be-130">-State</span><span class="sxs-lookup"><span data-stu-id="196be-130">-State</span></span>
<span data-ttu-id="196be-131">Określa stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="196be-131">Specifies the subscription state.</span></span>
<span data-ttu-id="196be-132">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="196be-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="196be-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="196be-133">-StateComment</span></span>
<span data-ttu-id="196be-134">Umożliwia określenie komentarza dotyczącego stanu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="196be-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="196be-135">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="196be-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="196be-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="196be-136">-SubscriptionId</span></span>
<span data-ttu-id="196be-137">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="196be-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="196be-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196be-138">CommonParameters</span></span>
<span data-ttu-id="196be-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="196be-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196be-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="196be-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196be-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="196be-141">INPUTS</span></span>

### <span data-ttu-id="196be-142">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="196be-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="196be-143">System. String</span><span class="sxs-lookup"><span data-stu-id="196be-143">System.String</span></span>

### <span data-ttu-id="196be-144">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementSubscriptionState, Microsoft. Azure. Commands. ApiManagement. servicemanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="196be-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="196be-145">System. Nullable "1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="196be-145">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="196be-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="196be-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="196be-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="196be-147">OUTPUTS</span></span>

### <span data-ttu-id="196be-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="196be-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="196be-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="196be-149">NOTES</span></span>

## <span data-ttu-id="196be-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="196be-150">RELATED LINKS</span></span>

[<span data-ttu-id="196be-151">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="196be-151">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="196be-152">Nowe — AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="196be-152">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="196be-153">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="196be-153">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


