---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 62c1bd394dd509b81a8ea748c26c0465718926c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552276"
---
# <span data-ttu-id="bd9de-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="bd9de-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="bd9de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd9de-102">SYNOPSIS</span></span>
<span data-ttu-id="bd9de-103">Umożliwia ustawienie istniejących szczegółów subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bd9de-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd9de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd9de-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd9de-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd9de-105">DESCRIPTION</span></span>
<span data-ttu-id="bd9de-106">Polecenie cmdlet **Set-AzureRmApiManagementSubscription** ustawia istniejące dane subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bd9de-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="bd9de-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd9de-107">EXAMPLES</span></span>

### <span data-ttu-id="bd9de-108">Przykład 1: Ustawianie kluczy stanów i podstawowych i pomocniczych dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bd9de-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="bd9de-109">To polecenie ustawia podstawowe i pomocnicze klucze subskrypcji oraz uaktywnia je.</span><span class="sxs-lookup"><span data-stu-id="bd9de-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="bd9de-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd9de-110">PARAMETERS</span></span>

### <span data-ttu-id="bd9de-111">-Context</span><span class="sxs-lookup"><span data-stu-id="bd9de-111">-Context</span></span>
<span data-ttu-id="bd9de-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="bd9de-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd9de-113">-DefaultProfile</span></span>
<span data-ttu-id="bd9de-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd9de-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="bd9de-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="bd9de-115">-ExpiresOn</span></span>
<span data-ttu-id="bd9de-116">Określa datę wygaśnięcia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bd9de-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="bd9de-117">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="bd9de-117">The default value of this parameter is $Null.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9de-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd9de-118">-Name</span></span>
<span data-ttu-id="bd9de-119">Określa nazwę subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bd9de-119">Specifies a subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9de-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd9de-120">-PassThru</span></span>
<span data-ttu-id="bd9de-121">passthru</span><span class="sxs-lookup"><span data-stu-id="bd9de-121">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9de-122">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="bd9de-122">-PrimaryKey</span></span>
<span data-ttu-id="bd9de-123">Określa klucz podstawowy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bd9de-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="bd9de-124">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="bd9de-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="bd9de-125">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="bd9de-125">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9de-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="bd9de-126">-SecondaryKey</span></span>
<span data-ttu-id="bd9de-127">Określa klucz pomocniczy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bd9de-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="bd9de-128">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="bd9de-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="bd9de-129">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="bd9de-129">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9de-130">-State</span><span class="sxs-lookup"><span data-stu-id="bd9de-130">-State</span></span>
<span data-ttu-id="bd9de-131">Określa stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="bd9de-131">Specifies the subscription state.</span></span>
<span data-ttu-id="bd9de-132">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="bd9de-132">The default value of this parameter is $Null.</span></span>

```yaml
Type: PsApiManagementSubscriptionState
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9de-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="bd9de-133">-StateComment</span></span>
<span data-ttu-id="bd9de-134">Umożliwia określenie komentarza dotyczącego stanu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bd9de-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="bd9de-135">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="bd9de-135">The default value of this parameter is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9de-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bd9de-136">-SubscriptionId</span></span>
<span data-ttu-id="bd9de-137">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bd9de-137">Specifies the subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9de-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd9de-138">CommonParameters</span></span>
<span data-ttu-id="bd9de-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd9de-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd9de-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd9de-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd9de-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd9de-141">INPUTS</span></span>

### <span data-ttu-id="bd9de-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bd9de-142">None</span></span>
<span data-ttu-id="bd9de-143">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="bd9de-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd9de-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd9de-144">OUTPUTS</span></span>

### <span data-ttu-id="bd9de-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="bd9de-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="bd9de-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd9de-146">NOTES</span></span>

## <span data-ttu-id="bd9de-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd9de-147">RELATED LINKS</span></span>

[<span data-ttu-id="bd9de-148">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="bd9de-148">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="bd9de-149">Nowe — AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="bd9de-149">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="bd9de-150">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="bd9de-150">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


