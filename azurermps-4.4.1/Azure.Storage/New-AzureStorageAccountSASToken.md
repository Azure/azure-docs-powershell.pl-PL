---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 8b280a13e7eb7a2e6ea3f52b4a121f313504b2ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525850"
---
# <span data-ttu-id="c2c4d-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="c2c4d-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="c2c4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c4d-103">Umożliwia utworzenie tokenu SAS na poziomie konta.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2c4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2c4d-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2c4d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="c2c4d-106">Polecenie cmdlet **New-AzureStorageSASToken** umożliwia utworzenie tokenu SAS (Shared Access Signature) na poziomie konta dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="c2c4d-107">Tokena SAS można używać do delegowania uprawnień dla wielu usług lub do delegowania uprawnień dla usług niedostępnych z tokenem SAS na poziomie obiektu.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="c2c4d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2c4d-108">EXAMPLES</span></span>

### <span data-ttu-id="c2c4d-109">Przykład 1. Tworzenie tokenu SAS na poziomie konta z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="c2c4d-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="c2c4d-110">To polecenie tworzy token SAS na poziomie konta z pełnymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="c2c4d-111">Przykład 2: Tworzenie tokenu SAS na poziomie konta dla zakresu adresów IP</span><span class="sxs-lookup"><span data-stu-id="c2c4d-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="c2c4d-112">To polecenie tworzy token SAS na poziomie konta dla żądań dotyczących tylko HTTPS z określonego zakresu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="c2c4d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2c4d-113">PARAMETERS</span></span>

### <span data-ttu-id="c2c4d-114">-Context</span><span class="sxs-lookup"><span data-stu-id="c2c4d-114">-Context</span></span>
<span data-ttu-id="c2c4d-115">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c2c4d-116">Możesz użyć polecenia cmdlet New-AzureStorageContext, aby uzyskać obiekt **AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="c2c4d-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="c2c4d-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c2c4d-117">-ExpiryTime</span></span>
<span data-ttu-id="c2c4d-118">Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="c2c4d-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c2c4d-119">-IPAddressOrRange</span></span>
<span data-ttu-id="c2c4d-120">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c2c4d-121">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-121">The range is inclusive.</span></span>

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

### <span data-ttu-id="c2c4d-122">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="c2c4d-122">-Permission</span></span>
<span data-ttu-id="c2c4d-123">Określa uprawnienia do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="c2c4d-124">Uprawnienia są ważne tylko wtedy, gdy pasują do określonego typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="c2c4d-125">Aby uzyskać więcej informacji na temat dopuszczalnych wartości uprawnień, zobacz konstruowanie skojarzeń zabezpieczeń kontahttps://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="c2c4d-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="c2c4d-126">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="c2c4d-126">-Protocol</span></span>
<span data-ttu-id="c2c4d-127">Umożliwia określenie protokołu dozwolonego dla żądania wykonywanego za pomocą skojarzeń zabezpieczeń konta.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="c2c4d-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c2c4d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2c4d-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c2c4d-129">HttpsOnly</span></span>
- <span data-ttu-id="c2c4d-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="c2c4d-130">HttpsOrHttp</span></span>

<span data-ttu-id="c2c4d-131">Wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-131">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="c2c4d-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c2c4d-132">-ResourceType</span></span>
<span data-ttu-id="c2c4d-133">Określa typy zasobów dostępne w tokenie SAS.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="c2c4d-134">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c2c4d-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2c4d-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c2c4d-135">None</span></span>
- <span data-ttu-id="c2c4d-136">Służby</span><span class="sxs-lookup"><span data-stu-id="c2c4d-136">Service</span></span>
- <span data-ttu-id="c2c4d-137">Opakowaniu</span><span class="sxs-lookup"><span data-stu-id="c2c4d-137">Container</span></span>
- <span data-ttu-id="c2c4d-138">Stream</span><span class="sxs-lookup"><span data-stu-id="c2c4d-138">Object</span></span>

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

### <span data-ttu-id="c2c4d-139">-Service</span><span class="sxs-lookup"><span data-stu-id="c2c4d-139">-Service</span></span>
<span data-ttu-id="c2c4d-140">Określa usługę.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-140">Specifies the service.</span></span>
<span data-ttu-id="c2c4d-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c2c4d-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2c4d-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c2c4d-142">None</span></span>
- <span data-ttu-id="c2c4d-143">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="c2c4d-143">Blob</span></span>
- <span data-ttu-id="c2c4d-144">Plik</span><span class="sxs-lookup"><span data-stu-id="c2c4d-144">File</span></span>
- <span data-ttu-id="c2c4d-145">Wykonany</span><span class="sxs-lookup"><span data-stu-id="c2c4d-145">Queue</span></span>
- <span data-ttu-id="c2c4d-146">Tworząc</span><span class="sxs-lookup"><span data-stu-id="c2c4d-146">Table</span></span>

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

### <span data-ttu-id="c2c4d-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c2c4d-147">-StartTime</span></span>
<span data-ttu-id="c2c4d-148">Określa czas (w postaci obiektu **DateTime** ), po upływie którego te skojarzenia będą obowiązywać.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="c2c4d-149">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="c2c4d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c4d-150">CommonParameters</span></span>
<span data-ttu-id="c2c4d-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c4d-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2c4d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c4d-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2c4d-153">INPUTS</span></span>

### <span data-ttu-id="c2c4d-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c2c4d-154">IStorageContext</span></span>

<span data-ttu-id="c2c4d-155">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="c2c4d-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="c2c4d-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2c4d-156">OUTPUTS</span></span>

### <span data-ttu-id="c2c4d-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c2c4d-157">System.String</span></span>

## <span data-ttu-id="c2c4d-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2c4d-158">NOTES</span></span>

## <span data-ttu-id="c2c4d-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2c4d-159">RELATED LINKS</span></span>

[<span data-ttu-id="c2c4d-160">Nowe — AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c2c4d-160">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="c2c4d-161">Nowe — AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="c2c4d-161">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="c2c4d-162">Nowe — AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="c2c4d-162">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="c2c4d-163">Nowe — AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="c2c4d-163">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="c2c4d-164">Nowe — AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="c2c4d-164">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="c2c4d-165">Nowe — AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="c2c4d-165">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


