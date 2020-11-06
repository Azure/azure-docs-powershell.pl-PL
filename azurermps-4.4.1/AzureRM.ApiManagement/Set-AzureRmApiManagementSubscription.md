---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 3b6d07577a6df05a57ed7675f5d14c847e8c33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527745"
---
# <span data-ttu-id="0671a-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0671a-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="0671a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0671a-102">SYNOPSIS</span></span>
<span data-ttu-id="0671a-103">Umożliwia ustawienie istniejących szczegółów subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0671a-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0671a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0671a-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0671a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0671a-105">DESCRIPTION</span></span>
<span data-ttu-id="0671a-106">Polecenie cmdlet **Set-AzureRmApiManagementSubscription** ustawia istniejące dane subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0671a-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="0671a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0671a-107">EXAMPLES</span></span>

### <span data-ttu-id="0671a-108">Przykład 1: Ustawianie kluczy stanów i podstawowych i pomocniczych dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0671a-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SencondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="0671a-109">To polecenie ustawia podstawowe i pomocnicze klucze subskrypcji oraz uaktywnia je.</span><span class="sxs-lookup"><span data-stu-id="0671a-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="0671a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0671a-110">PARAMETERS</span></span>

### <span data-ttu-id="0671a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0671a-111">-Context</span></span>
<span data-ttu-id="0671a-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0671a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0671a-113">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="0671a-113">-ExpiresOn</span></span>
<span data-ttu-id="0671a-114">Określa datę wygaśnięcia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0671a-114">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="0671a-115">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="0671a-115">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="0671a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0671a-116">-Name</span></span>
<span data-ttu-id="0671a-117">Określa nazwę subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0671a-117">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="0671a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0671a-118">-PassThru</span></span>
<span data-ttu-id="0671a-119">passthru</span><span class="sxs-lookup"><span data-stu-id="0671a-119">passthru</span></span>

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

### <span data-ttu-id="0671a-120">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="0671a-120">-PrimaryKey</span></span>
<span data-ttu-id="0671a-121">Określa klucz podstawowy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0671a-121">Specifies the subscription primary key.</span></span>
<span data-ttu-id="0671a-122">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="0671a-122">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="0671a-123">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="0671a-123">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="0671a-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="0671a-124">-SecondaryKey</span></span>
<span data-ttu-id="0671a-125">Określa klucz pomocniczy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0671a-125">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="0671a-126">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="0671a-126">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="0671a-127">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="0671a-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="0671a-128">-State</span><span class="sxs-lookup"><span data-stu-id="0671a-128">-State</span></span>
<span data-ttu-id="0671a-129">Określa stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="0671a-129">Specifies the subscription state.</span></span>
<span data-ttu-id="0671a-130">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="0671a-130">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="0671a-131">-StateComment</span><span class="sxs-lookup"><span data-stu-id="0671a-131">-StateComment</span></span>
<span data-ttu-id="0671a-132">Umożliwia określenie komentarza dotyczącego stanu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0671a-132">Specifies the subscription state comment.</span></span>
<span data-ttu-id="0671a-133">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="0671a-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="0671a-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0671a-134">-SubscriptionId</span></span>
<span data-ttu-id="0671a-135">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0671a-135">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="0671a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0671a-136">-DefaultProfile</span></span>
<span data-ttu-id="0671a-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0671a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0671a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0671a-138">CommonParameters</span></span>
<span data-ttu-id="0671a-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0671a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0671a-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0671a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0671a-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0671a-141">INPUTS</span></span>

## <span data-ttu-id="0671a-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0671a-142">OUTPUTS</span></span>

### <span data-ttu-id="0671a-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="0671a-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="0671a-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0671a-144">NOTES</span></span>

## <span data-ttu-id="0671a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0671a-145">RELATED LINKS</span></span>

[<span data-ttu-id="0671a-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0671a-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="0671a-147">Nowe — AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0671a-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="0671a-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0671a-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


