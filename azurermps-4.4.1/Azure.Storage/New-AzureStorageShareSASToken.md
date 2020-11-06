---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 84f280bf5e3297796bb8b56e5a5d42e513b79e79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527769"
---
# <span data-ttu-id="d13dc-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="d13dc-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="d13dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d13dc-102">SYNOPSIS</span></span>
<span data-ttu-id="d13dc-103">Wygeneruj token podpisu dostępu współdzielonego dla udziału magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d13dc-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d13dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d13dc-104">SYNTAX</span></span>

### <span data-ttu-id="d13dc-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="d13dc-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="d13dc-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="d13dc-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d13dc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d13dc-107">DESCRIPTION</span></span>
<span data-ttu-id="d13dc-108">Polecenie cmdlet **New-AzureStorageShareSASToken** generuje token podpisu dostępu współdzielonego dla udziału w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d13dc-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="d13dc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d13dc-109">EXAMPLES</span></span>

### <span data-ttu-id="d13dc-110">Przykład 1. Wygeneruj token podpisu dostępu współdzielonego dla udziału</span><span class="sxs-lookup"><span data-stu-id="d13dc-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="d13dc-111">To polecenie tworzy token podpisu dostępu współdzielonego dla udziału o nazwie ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="d13dc-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="d13dc-112">Przykład 2: generowanie wielu tokenów podpisu dostępu współdzielonego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="d13dc-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="d13dc-113">To polecenie pobiera wszystkie udziały w magazynie, które pasują do testu prefiksu.</span><span class="sxs-lookup"><span data-stu-id="d13dc-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="d13dc-114">Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="d13dc-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d13dc-115">Bieżące polecenie cmdlet tworzy token dostępu współdzielonego dla każdego udziału miejsca do magazynowania, który ma określone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="d13dc-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="d13dc-116">Przykład 3: generowanie tokenu podpisu z dostępem udostępnionym korzystającym z zasad dostępu współużytkowanego</span><span class="sxs-lookup"><span data-stu-id="d13dc-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="d13dc-117">To polecenie tworzy token podpisu dostępu współdzielonego dla udziału magazynu o nazwie ContosoShare, który zawiera zasady o nazwie ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="d13dc-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="d13dc-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d13dc-118">PARAMETERS</span></span>

### <span data-ttu-id="d13dc-119">-Context</span><span class="sxs-lookup"><span data-stu-id="d13dc-119">-Context</span></span>
<span data-ttu-id="d13dc-120">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d13dc-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="d13dc-121">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d13dc-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d13dc-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d13dc-122">-ExpiryTime</span></span>
<span data-ttu-id="d13dc-123">Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="d13dc-123">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="d13dc-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="d13dc-124">-FullUri</span></span>
<span data-ttu-id="d13dc-125">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="d13dc-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13dc-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d13dc-126">-IPAddressOrRange</span></span>
<span data-ttu-id="d13dc-127">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="d13dc-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="d13dc-128">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="d13dc-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="d13dc-129">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="d13dc-129">-Permission</span></span>
<span data-ttu-id="d13dc-130">Określa uprawnienia w tokenie umożliwiające uzyskanie dostępu do udziału i plików w udziale.</span><span class="sxs-lookup"><span data-stu-id="d13dc-130">Specifies the permissions in the token to access the share and files under the share.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13dc-131">-Policy</span><span class="sxs-lookup"><span data-stu-id="d13dc-131">-Policy</span></span>
<span data-ttu-id="d13dc-132">Określa zapisane zasady dostępu dla udziału.</span><span class="sxs-lookup"><span data-stu-id="d13dc-132">Specifies the stored access policy for a share.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13dc-133">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="d13dc-133">-Protocol</span></span>
<span data-ttu-id="d13dc-134">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="d13dc-134">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="d13dc-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d13dc-135">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="d13dc-136">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d13dc-136">HttpsOnly</span></span>
* <span data-ttu-id="d13dc-137">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="d13dc-137">HttpsOrHttp</span></span>

<span data-ttu-id="d13dc-138">Wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="d13dc-138">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="d13dc-139">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="d13dc-139">-ShareName</span></span>
<span data-ttu-id="d13dc-140">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="d13dc-140">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d13dc-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d13dc-141">-StartTime</span></span>
<span data-ttu-id="d13dc-142">Określa czas, po upływie którego podpis udostępniony będzie ważny.</span><span class="sxs-lookup"><span data-stu-id="d13dc-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="d13dc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13dc-143">CommonParameters</span></span>
<span data-ttu-id="d13dc-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d13dc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13dc-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d13dc-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13dc-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d13dc-146">INPUTS</span></span>

### <span data-ttu-id="d13dc-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d13dc-147">IStorageContext</span></span>

<span data-ttu-id="d13dc-148">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="d13dc-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="d13dc-149">Ciąg</span><span class="sxs-lookup"><span data-stu-id="d13dc-149">String</span></span>

<span data-ttu-id="d13dc-150">Parametr "nazwa_udziału" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="d13dc-150">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d13dc-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d13dc-151">OUTPUTS</span></span>

### <span data-ttu-id="d13dc-152">System. String</span><span class="sxs-lookup"><span data-stu-id="d13dc-152">System.String</span></span>

## <span data-ttu-id="d13dc-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d13dc-153">NOTES</span></span>
* <span data-ttu-id="d13dc-154">Słowa kluczowe: typowe, Azure, usługi, dane, przechowywanie, obiekt BLOB, kolejka, tabela</span><span class="sxs-lookup"><span data-stu-id="d13dc-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="d13dc-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d13dc-155">RELATED LINKS</span></span>

[<span data-ttu-id="d13dc-156">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="d13dc-156">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="d13dc-157">Nowe — AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="d13dc-157">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)
