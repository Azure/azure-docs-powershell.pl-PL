---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
ms.openlocfilehash: 8b0eb67808bf4148d93006b24273d55b737adfea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547800"
---
# <span data-ttu-id="d22e8-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="d22e8-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="d22e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d22e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d22e8-103">Umożliwia utworzenie tokenu SAS na poziomie konta.</span><span class="sxs-lookup"><span data-stu-id="d22e8-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d22e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d22e8-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d22e8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d22e8-105">DESCRIPTION</span></span>
<span data-ttu-id="d22e8-106">Polecenie cmdlet **New-AzureStorageSASToken** umożliwia utworzenie tokenu SAS (Shared Access Signature) na poziomie konta dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d22e8-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="d22e8-107">Tokena SAS można używać do delegowania uprawnień dla wielu usług lub do delegowania uprawnień dla usług niedostępnych z tokenem SAS na poziomie obiektu.</span><span class="sxs-lookup"><span data-stu-id="d22e8-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="d22e8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d22e8-108">EXAMPLES</span></span>

### <span data-ttu-id="d22e8-109">Przykład 1. Tworzenie tokenu SAS na poziomie konta z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="d22e8-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="d22e8-110">To polecenie tworzy token SAS na poziomie konta z pełnymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="d22e8-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="d22e8-111">Przykład 2: Tworzenie tokenu SAS na poziomie konta dla zakresu adresów IP</span><span class="sxs-lookup"><span data-stu-id="d22e8-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="d22e8-112">To polecenie tworzy token SAS na poziomie konta dla żądań dotyczących tylko HTTPS z określonego zakresu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="d22e8-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="d22e8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d22e8-113">PARAMETERS</span></span>

### <span data-ttu-id="d22e8-114">-Context</span><span class="sxs-lookup"><span data-stu-id="d22e8-114">-Context</span></span>
<span data-ttu-id="d22e8-115">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d22e8-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d22e8-116">Możesz użyć polecenia cmdlet New-AzureStorageContext, aby uzyskać obiekt **AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="d22e8-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d22e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22e8-117">-DefaultProfile</span></span>
<span data-ttu-id="d22e8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d22e8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d22e8-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d22e8-119">-ExpiryTime</span></span>
<span data-ttu-id="d22e8-120">Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="d22e8-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22e8-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d22e8-121">-IPAddressOrRange</span></span>
<span data-ttu-id="d22e8-122">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="d22e8-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="d22e8-123">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="d22e8-123">The range is inclusive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22e8-124">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="d22e8-124">-Permission</span></span>
<span data-ttu-id="d22e8-125">Określa uprawnienia do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d22e8-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="d22e8-126">Uprawnienia są ważne tylko wtedy, gdy pasują do określonego typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="d22e8-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="d22e8-127">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="d22e8-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="d22e8-128">Aby uzyskać więcej informacji na temat dopuszczalnych wartości uprawnień, zobacz konstruowanie skojarzeń zabezpieczeń konta https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="d22e8-128">For more information about acceptable permission values, see Constructing an Account SAS https://go.microsoft.com/fwlink/?LinkId=799514</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22e8-129">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="d22e8-129">-Protocol</span></span>
<span data-ttu-id="d22e8-130">Umożliwia określenie protokołu dozwolonego dla żądania wykonywanego za pomocą skojarzeń zabezpieczeń konta.</span><span class="sxs-lookup"><span data-stu-id="d22e8-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="d22e8-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d22e8-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d22e8-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d22e8-132">HttpsOnly</span></span>
- <span data-ttu-id="d22e8-133">HttpsOrHttp wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="d22e8-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22e8-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d22e8-134">-ResourceType</span></span>
<span data-ttu-id="d22e8-135">Określa typy zasobów dostępne w tokenie SAS.</span><span class="sxs-lookup"><span data-stu-id="d22e8-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="d22e8-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d22e8-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d22e8-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d22e8-137">None</span></span>
- <span data-ttu-id="d22e8-138">Służby</span><span class="sxs-lookup"><span data-stu-id="d22e8-138">Service</span></span>
- <span data-ttu-id="d22e8-139">Opakowaniu</span><span class="sxs-lookup"><span data-stu-id="d22e8-139">Container</span></span>
- <span data-ttu-id="d22e8-140">Stream</span><span class="sxs-lookup"><span data-stu-id="d22e8-140">Object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22e8-141">-Service</span><span class="sxs-lookup"><span data-stu-id="d22e8-141">-Service</span></span>
<span data-ttu-id="d22e8-142">Określa usługę.</span><span class="sxs-lookup"><span data-stu-id="d22e8-142">Specifies the service.</span></span>
<span data-ttu-id="d22e8-143">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d22e8-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d22e8-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d22e8-144">None</span></span>
- <span data-ttu-id="d22e8-145">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="d22e8-145">Blob</span></span>
- <span data-ttu-id="d22e8-146">Plik</span><span class="sxs-lookup"><span data-stu-id="d22e8-146">File</span></span>
- <span data-ttu-id="d22e8-147">Wykonany</span><span class="sxs-lookup"><span data-stu-id="d22e8-147">Queue</span></span>
- <span data-ttu-id="d22e8-148">Tworząc</span><span class="sxs-lookup"><span data-stu-id="d22e8-148">Table</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22e8-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d22e8-149">-StartTime</span></span>
<span data-ttu-id="d22e8-150">Określa czas (w postaci obiektu **DateTime** ), po upływie którego te skojarzenia będą obowiązywać.</span><span class="sxs-lookup"><span data-stu-id="d22e8-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="d22e8-151">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="d22e8-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22e8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22e8-152">CommonParameters</span></span>
<span data-ttu-id="d22e8-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22e8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22e8-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d22e8-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22e8-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d22e8-155">INPUTS</span></span>

### <span data-ttu-id="d22e8-156">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d22e8-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d22e8-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d22e8-157">OUTPUTS</span></span>

### <span data-ttu-id="d22e8-158">System. String</span><span class="sxs-lookup"><span data-stu-id="d22e8-158">System.String</span></span>

## <span data-ttu-id="d22e8-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d22e8-159">NOTES</span></span>

## <span data-ttu-id="d22e8-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d22e8-160">RELATED LINKS</span></span>

[<span data-ttu-id="d22e8-161">Nowe — AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d22e8-161">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="d22e8-162">Nowe — AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d22e8-162">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="d22e8-163">Nowe — AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="d22e8-163">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="d22e8-164">Nowe — AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="d22e8-164">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="d22e8-165">Nowe — AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="d22e8-165">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="d22e8-166">Nowe — AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="d22e8-166">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


