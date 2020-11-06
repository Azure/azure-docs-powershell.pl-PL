---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
ms.openlocfilehash: 427276a496108a48b69fd81cb5835d74859c25b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523565"
---
# <span data-ttu-id="f1f7e-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="f1f7e-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="f1f7e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f7e-103">Wygeneruj token podpisu dostępu współdzielonego dla udziału magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="f1f7e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1f7e-104">SYNTAX</span></span>

### <span data-ttu-id="f1f7e-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="f1f7e-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="f1f7e-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="f1f7e-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="f1f7e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f1f7e-107">DESCRIPTION</span></span>
<span data-ttu-id="f1f7e-108">Polecenie cmdlet **New-AzureStorageShareSASToken** generuje token podpisu dostępu współdzielonego dla udziału w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="f1f7e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1f7e-109">EXAMPLES</span></span>

### <span data-ttu-id="f1f7e-110">Przykład 1. Wygeneruj token podpisu dostępu współdzielonego dla udziału</span><span class="sxs-lookup"><span data-stu-id="f1f7e-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="f1f7e-111">To polecenie tworzy token podpisu dostępu współdzielonego dla udziału o nazwie ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="f1f7e-112">Przykład 2: generowanie wielu tokenów podpisu dostępu współdzielonego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="f1f7e-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="f1f7e-113">To polecenie pobiera wszystkie udziały w magazynie, które pasują do testu prefiksu.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="f1f7e-114">Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f1f7e-115">Bieżące polecenie cmdlet tworzy token dostępu współdzielonego dla każdego udziału miejsca do magazynowania, który ma określone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="f1f7e-116">Przykład 3: generowanie tokenu podpisu z dostępem udostępnionym korzystającym z zasad dostępu współużytkowanego</span><span class="sxs-lookup"><span data-stu-id="f1f7e-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="f1f7e-117">To polecenie tworzy token podpisu dostępu współdzielonego dla udziału magazynu o nazwie ContosoShare, który zawiera zasady o nazwie ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="f1f7e-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1f7e-118">PARAMETERS</span></span>

### <span data-ttu-id="f1f7e-119">-Context</span><span class="sxs-lookup"><span data-stu-id="f1f7e-119">-Context</span></span>
<span data-ttu-id="f1f7e-120">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f1f7e-121">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f1f7e-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f1f7e-122">-ExpiryTime</span></span>
<span data-ttu-id="f1f7e-123">Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-123">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="f1f7e-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="f1f7e-124">-FullUri</span></span>
<span data-ttu-id="f1f7e-125">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="f1f7e-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f1f7e-126">-IPAddressOrRange</span></span>
<span data-ttu-id="f1f7e-127">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="f1f7e-128">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="f1f7e-129">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="f1f7e-129">-Permission</span></span>
<span data-ttu-id="f1f7e-130">Określa uprawnienia w tokenie umożliwiające uzyskanie dostępu do udziału i plików w udziale.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-130">Specifies the permissions in the token to access the share and files under the share.</span></span>

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

### <span data-ttu-id="f1f7e-131">-Policy</span><span class="sxs-lookup"><span data-stu-id="f1f7e-131">-Policy</span></span>
<span data-ttu-id="f1f7e-132">Określa zapisane zasady dostępu dla udziału.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-132">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="f1f7e-133">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="f1f7e-133">-Protocol</span></span>
<span data-ttu-id="f1f7e-134">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-134">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="f1f7e-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f1f7e-135">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="f1f7e-136">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f1f7e-136">HttpsOnly</span></span>
* <span data-ttu-id="f1f7e-137">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="f1f7e-137">HttpsOrHttp</span></span>

<span data-ttu-id="f1f7e-138">Wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-138">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="f1f7e-139">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="f1f7e-139">-ShareName</span></span>
<span data-ttu-id="f1f7e-140">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="f1f7e-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f1f7e-141">-StartTime</span></span>
<span data-ttu-id="f1f7e-142">Określa czas, po upływie którego podpis udostępniony będzie ważny.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="f1f7e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f7e-143">CommonParameters</span></span>
<span data-ttu-id="f1f7e-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f7e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f7e-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f7e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f7e-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1f7e-146">INPUTS</span></span>

## <span data-ttu-id="f1f7e-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1f7e-147">OUTPUTS</span></span>

## <span data-ttu-id="f1f7e-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1f7e-148">NOTES</span></span>
* <span data-ttu-id="f1f7e-149">Słowa kluczowe: typowe, Azure, usługi, dane, przechowywanie, obiekt BLOB, kolejka, tabela</span><span class="sxs-lookup"><span data-stu-id="f1f7e-149">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="f1f7e-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1f7e-150">RELATED LINKS</span></span>

[<span data-ttu-id="f1f7e-151">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1f7e-151">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="f1f7e-152">Nowe — AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="f1f7e-152">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)
