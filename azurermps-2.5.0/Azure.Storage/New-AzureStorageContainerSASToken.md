---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainersastoken
schema: 2.0.0
ms.openlocfilehash: 3fa5a642bd5d8c53b81422f54fdb2c133304cc03
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899412"
---
# <span data-ttu-id="8d354-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="8d354-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="8d354-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d354-102">SYNOPSIS</span></span>
<span data-ttu-id="8d354-103">Generuje token SAS dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8d354-103">Generates an SAS token for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d354-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d354-104">SYNTAX</span></span>

### <span data-ttu-id="8d354-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="8d354-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d354-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="8d354-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d354-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8d354-107">DESCRIPTION</span></span>
<span data-ttu-id="8d354-108">Polecenie cmdlet **New-AzureStorageContainerSASToken** generuje token dostępu współużytkowanego (SAS) dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8d354-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="8d354-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d354-109">EXAMPLES</span></span>

### <span data-ttu-id="8d354-110">Przykład 1. Generuj token SAS kontenera z uprawnieniem pełny kontener</span><span class="sxs-lookup"><span data-stu-id="8d354-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="8d354-111">W tym przykładzie Wygenerowano token SAS kontenera z uprawnieniem pełnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="8d354-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="8d354-112">Przykład 2: generowanie wielu tokenów SAS kontenera według rurociągu</span><span class="sxs-lookup"><span data-stu-id="8d354-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="8d354-113">W tym przykładzie Wygenerowano wiele tokenów SAS kontenera za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="8d354-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="8d354-114">Przykład 3: generowanie tokenu SAS kontenera z zasadami dostępu współużytkowanego</span><span class="sxs-lookup"><span data-stu-id="8d354-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="8d354-115">W tym przykładzie Wygenerowano token SAS kontenera z zasadami dostępu współużytkowanego.</span><span class="sxs-lookup"><span data-stu-id="8d354-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="8d354-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d354-116">PARAMETERS</span></span>

### <span data-ttu-id="8d354-117">-Context</span><span class="sxs-lookup"><span data-stu-id="8d354-117">-Context</span></span>
<span data-ttu-id="8d354-118">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8d354-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8d354-119">Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="8d354-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8d354-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d354-120">-DefaultProfile</span></span>
<span data-ttu-id="8d354-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d354-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d354-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8d354-122">-ExpiryTime</span></span>
<span data-ttu-id="8d354-123">Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="8d354-123">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="8d354-124">Jeśli użytkownik ustawi czas rozpoczęcia, ale nie czas wygaśnięcia, czas wygaśnięcia jest ustawiany na czas rozpoczęcia Plus o godzinę.</span><span class="sxs-lookup"><span data-stu-id="8d354-124">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="8d354-125">Jeśli nie określono godziny rozpoczęcia ani godziny wygaśnięcia, czas wygaśnięcia jest ustawiany na bieżący czas plus co godzinę.</span><span class="sxs-lookup"><span data-stu-id="8d354-125">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="8d354-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="8d354-126">-FullUri</span></span>
<span data-ttu-id="8d354-127">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="8d354-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="8d354-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8d354-128">-IPAddressOrRange</span></span>
<span data-ttu-id="8d354-129">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="8d354-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="8d354-130">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="8d354-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="8d354-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8d354-131">-Name</span></span>
<span data-ttu-id="8d354-132">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8d354-132">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d354-133">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="8d354-133">-Permission</span></span>
<span data-ttu-id="8d354-134">Określa uprawnienia kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="8d354-134">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="8d354-135">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="8d354-135">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="8d354-136">-Policy</span><span class="sxs-lookup"><span data-stu-id="8d354-136">-Policy</span></span>
<span data-ttu-id="8d354-137">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8d354-137">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="8d354-138">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="8d354-138">-Protocol</span></span>
<span data-ttu-id="8d354-139">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="8d354-139">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="8d354-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8d354-140">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="8d354-141">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8d354-141">HttpsOnly</span></span>
* <span data-ttu-id="8d354-142">HttpsOrHttp wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="8d354-142">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="8d354-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8d354-143">-StartTime</span></span>
<span data-ttu-id="8d354-144">Określa czas, po upływie którego podpis udostępniony będzie ważny.</span><span class="sxs-lookup"><span data-stu-id="8d354-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="8d354-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d354-145">CommonParameters</span></span>
<span data-ttu-id="8d354-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d354-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d354-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d354-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d354-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d354-148">INPUTS</span></span>

### <span data-ttu-id="8d354-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8d354-149">System.String</span></span>

### <span data-ttu-id="8d354-150">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d354-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8d354-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d354-151">OUTPUTS</span></span>

### <span data-ttu-id="8d354-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8d354-152">System.String</span></span>

## <span data-ttu-id="8d354-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d354-153">NOTES</span></span>

## <span data-ttu-id="8d354-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d354-154">RELATED LINKS</span></span>

[<span data-ttu-id="8d354-155">Nowe — AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8d354-155">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
