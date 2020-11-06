---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c888c5e7a4083fd91fdddfd6d2442cb65056d42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523990"
---
# <span data-ttu-id="b5d24-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="b5d24-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="b5d24-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5d24-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d24-103">Tworzy token SAS.</span><span class="sxs-lookup"><span data-stu-id="b5d24-103">Creates an SAS token.</span></span>

## <span data-ttu-id="b5d24-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5d24-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5d24-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5d24-105">DESCRIPTION</span></span>
<span data-ttu-id="b5d24-106">Polecenie cmdlet **New-AzureStorageSASToken** umożliwia utworzenie tokenu SAS (Shared Access Signature) na poziomie konta dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b5d24-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="b5d24-107">Tokena SAS można używać do delegowania uprawnień dla wielu usług lub do delegowania uprawnień dla usług niedostępnych z tokenem SAS na poziomie obiektu.</span><span class="sxs-lookup"><span data-stu-id="b5d24-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="b5d24-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5d24-108">EXAMPLES</span></span>

### <span data-ttu-id="b5d24-109">Przykład 1. Tworzenie tokenu SAS</span><span class="sxs-lookup"><span data-stu-id="b5d24-109">Example 1: Create an SAS token</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="b5d24-110">To polecenie tworzy token SAS na poziomie konta z pełnymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="b5d24-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="b5d24-111">Przykład 2: Tworzenie tokenu SAS dla zakresu adresów IP</span><span class="sxs-lookup"><span data-stu-id="b5d24-111">Example 2: Create an SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="b5d24-112">To polecenie tworzy token SAS dla żądań tylko HTTPS z określonego zakresu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b5d24-112">This command creates an SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="b5d24-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5d24-113">PARAMETERS</span></span>

### <span data-ttu-id="b5d24-114">-Context</span><span class="sxs-lookup"><span data-stu-id="b5d24-114">-Context</span></span>
<span data-ttu-id="b5d24-115">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b5d24-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b5d24-116">Możesz użyć polecenia cmdlet New-AzureStorageContext, aby uzyskać obiekt **AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="b5d24-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d24-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b5d24-117">-ExpiryTime</span></span>
<span data-ttu-id="b5d24-118">Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="b5d24-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d24-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b5d24-119">-IPAddressOrRange</span></span>
<span data-ttu-id="b5d24-120">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="b5d24-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="b5d24-121">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="b5d24-121">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d24-122">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="b5d24-122">-Permission</span></span>
<span data-ttu-id="b5d24-123">Określa uprawnienia do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b5d24-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="b5d24-124">Uprawnienia są ważne tylko wtedy, gdy pasują do określonego typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="b5d24-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="b5d24-125">Aby uzyskać więcej informacji na temat dopuszczalnych wartości uprawnień, zobacz konstruowanie skojarzeń zabezpieczeń kontahttps://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="b5d24-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d24-126">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="b5d24-126">-Protocol</span></span>
<span data-ttu-id="b5d24-127">Umożliwia określenie protokołu dozwolonego dla żądania wykonywanego za pomocą skojarzeń zabezpieczeń konta.</span><span class="sxs-lookup"><span data-stu-id="b5d24-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="b5d24-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b5d24-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5d24-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b5d24-129">HttpsOnly</span></span>
- <span data-ttu-id="b5d24-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="b5d24-130">HttpsOrHttp</span></span>

<span data-ttu-id="b5d24-131">Wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="b5d24-131">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d24-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b5d24-132">-ResourceType</span></span>
<span data-ttu-id="b5d24-133">Określa typy zasobów dostępne w tokenie SAS.</span><span class="sxs-lookup"><span data-stu-id="b5d24-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="b5d24-134">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b5d24-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5d24-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b5d24-135">None</span></span>
- <span data-ttu-id="b5d24-136">Służby</span><span class="sxs-lookup"><span data-stu-id="b5d24-136">Service</span></span>
- <span data-ttu-id="b5d24-137">Opakowaniu</span><span class="sxs-lookup"><span data-stu-id="b5d24-137">Container</span></span>
- <span data-ttu-id="b5d24-138">Stream</span><span class="sxs-lookup"><span data-stu-id="b5d24-138">Object</span></span>

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d24-139">-Service</span><span class="sxs-lookup"><span data-stu-id="b5d24-139">-Service</span></span>
<span data-ttu-id="b5d24-140">Określa usługę.</span><span class="sxs-lookup"><span data-stu-id="b5d24-140">Specifies the service.</span></span>
<span data-ttu-id="b5d24-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b5d24-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5d24-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b5d24-142">None</span></span>
- <span data-ttu-id="b5d24-143">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="b5d24-143">Blob</span></span>
- <span data-ttu-id="b5d24-144">Plik</span><span class="sxs-lookup"><span data-stu-id="b5d24-144">File</span></span>
- <span data-ttu-id="b5d24-145">Wykonany</span><span class="sxs-lookup"><span data-stu-id="b5d24-145">Queue</span></span>
- <span data-ttu-id="b5d24-146">Tworząc</span><span class="sxs-lookup"><span data-stu-id="b5d24-146">Table</span></span>

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d24-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b5d24-147">-StartTime</span></span>
<span data-ttu-id="b5d24-148">Określa czas (w postaci obiektu **DateTime** ), po upływie którego te skojarzenia będą obowiązywać.</span><span class="sxs-lookup"><span data-stu-id="b5d24-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="b5d24-149">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="b5d24-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d24-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d24-150">CommonParameters</span></span>
<span data-ttu-id="b5d24-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5d24-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d24-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5d24-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d24-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5d24-153">INPUTS</span></span>

## <span data-ttu-id="b5d24-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5d24-154">OUTPUTS</span></span>

## <span data-ttu-id="b5d24-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5d24-155">NOTES</span></span>

## <span data-ttu-id="b5d24-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5d24-156">RELATED LINKS</span></span>

[<span data-ttu-id="b5d24-157">Nowe — AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b5d24-157">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="b5d24-158">Nowe — AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="b5d24-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="b5d24-159">Nowe — AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="b5d24-159">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="b5d24-160">Nowe — AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="b5d24-160">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="b5d24-161">Nowe — AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="b5d24-161">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="b5d24-162">Nowe — AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="b5d24-162">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


