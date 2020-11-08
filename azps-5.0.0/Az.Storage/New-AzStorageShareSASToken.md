---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233817"
---
# <span data-ttu-id="1026a-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="1026a-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="1026a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1026a-102">SYNOPSIS</span></span>
<span data-ttu-id="1026a-103">Wygeneruj token podpisu dostępu współdzielonego dla udziału magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1026a-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="1026a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1026a-104">SYNTAX</span></span>

### <span data-ttu-id="1026a-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="1026a-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1026a-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="1026a-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1026a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1026a-107">DESCRIPTION</span></span>
<span data-ttu-id="1026a-108">Polecenie cmdlet **New-AzStorageShareSASToken** generuje token podpisu dostępu współdzielonego dla udziału w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1026a-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="1026a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1026a-109">EXAMPLES</span></span>

### <span data-ttu-id="1026a-110">Przykład 1. Wygeneruj token podpisu dostępu współdzielonego dla udziału</span><span class="sxs-lookup"><span data-stu-id="1026a-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="1026a-111">To polecenie tworzy token podpisu dostępu współdzielonego dla udziału o nazwie ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="1026a-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="1026a-112">Przykład 2: generowanie wielu tokenów podpisu dostępu współdzielonego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="1026a-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="1026a-113">To polecenie pobiera wszystkie udziały w magazynie, które pasują do testu prefiksu.</span><span class="sxs-lookup"><span data-stu-id="1026a-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="1026a-114">Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="1026a-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1026a-115">Bieżące polecenie cmdlet tworzy token dostępu współdzielonego dla każdego udziału miejsca do magazynowania, który ma określone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="1026a-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="1026a-116">Przykład 3: generowanie tokenu podpisu z dostępem udostępnionym korzystającym z zasad dostępu współużytkowanego</span><span class="sxs-lookup"><span data-stu-id="1026a-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="1026a-117">To polecenie tworzy token podpisu dostępu współdzielonego dla udziału magazynu o nazwie ContosoShare, który zawiera zasady o nazwie ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="1026a-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="1026a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1026a-118">PARAMETERS</span></span>

### <span data-ttu-id="1026a-119">-Context</span><span class="sxs-lookup"><span data-stu-id="1026a-119">-Context</span></span>
<span data-ttu-id="1026a-120">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1026a-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="1026a-121">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1026a-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1026a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1026a-122">-DefaultProfile</span></span>
<span data-ttu-id="1026a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1026a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1026a-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1026a-124">-ExpiryTime</span></span>
<span data-ttu-id="1026a-125">Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="1026a-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="1026a-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="1026a-126">-FullUri</span></span>
<span data-ttu-id="1026a-127">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="1026a-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1026a-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1026a-128">-IPAddressOrRange</span></span>
<span data-ttu-id="1026a-129">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="1026a-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="1026a-130">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="1026a-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="1026a-131">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="1026a-131">-Permission</span></span>
<span data-ttu-id="1026a-132">Określa uprawnienia w tokenie umożliwiające uzyskanie dostępu do udziału i plików w udziale.</span><span class="sxs-lookup"><span data-stu-id="1026a-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="1026a-133">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="1026a-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1026a-134">-Policy</span><span class="sxs-lookup"><span data-stu-id="1026a-134">-Policy</span></span>
<span data-ttu-id="1026a-135">Określa zapisane zasady dostępu dla udziału.</span><span class="sxs-lookup"><span data-stu-id="1026a-135">Specifies the stored access policy for a share.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1026a-136">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="1026a-136">-Protocol</span></span>
<span data-ttu-id="1026a-137">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="1026a-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="1026a-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1026a-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="1026a-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1026a-139">HttpsOnly</span></span>
* <span data-ttu-id="1026a-140">HttpsOrHttp wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="1026a-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1026a-141">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="1026a-141">-ShareName</span></span>
<span data-ttu-id="1026a-142">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="1026a-142">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1026a-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1026a-143">-StartTime</span></span>
<span data-ttu-id="1026a-144">Określa czas, po upływie którego podpis udostępniony będzie ważny.</span><span class="sxs-lookup"><span data-stu-id="1026a-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="1026a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1026a-145">CommonParameters</span></span>
<span data-ttu-id="1026a-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1026a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1026a-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1026a-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1026a-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1026a-148">INPUTS</span></span>

### <span data-ttu-id="1026a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="1026a-149">System.String</span></span>

### <span data-ttu-id="1026a-150">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1026a-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1026a-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1026a-151">OUTPUTS</span></span>

### <span data-ttu-id="1026a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="1026a-152">System.String</span></span>

## <span data-ttu-id="1026a-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1026a-153">NOTES</span></span>
* <span data-ttu-id="1026a-154">Słowa kluczowe: typowe, Azure, usługi, dane, przechowywanie, obiekt BLOB, kolejka, tabela</span><span class="sxs-lookup"><span data-stu-id="1026a-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="1026a-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1026a-155">RELATED LINKS</span></span>

[<span data-ttu-id="1026a-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="1026a-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="1026a-157">Nowe — AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="1026a-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
