---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
ms.openlocfilehash: 76ed7737acb26cd713aa84b26a743f3e5e43874f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717134"
---
# <span data-ttu-id="f95e9-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="f95e9-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="f95e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f95e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f95e9-103">Generuje token SAS dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f95e9-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f95e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f95e9-104">SYNTAX</span></span>

### <span data-ttu-id="f95e9-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="f95e9-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="f95e9-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="f95e9-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="f95e9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f95e9-107">DESCRIPTION</span></span>
<span data-ttu-id="f95e9-108">Polecenie cmdlet **New-AzureStorageTableSASToken** generuje token dostępu współużytkowanego (SAS) dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f95e9-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="f95e9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f95e9-109">EXAMPLES</span></span>

### <span data-ttu-id="f95e9-110">Przykład 1. Generuj token SAS z pełnymi uprawnieniami dla tabeli</span><span class="sxs-lookup"><span data-stu-id="f95e9-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="f95e9-111">To polecenie generuje token SAS z pełnymi uprawnieniami dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="f95e9-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="f95e9-112">Token ten jest przeznaczony dla uprawnień Odczyt, Dodawanie, aktualizowanie i usuwanie.</span><span class="sxs-lookup"><span data-stu-id="f95e9-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="f95e9-113">Przykład 2: generowanie tokenu SAS dla zakresu partycji</span><span class="sxs-lookup"><span data-stu-id="f95e9-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="f95e9-114">To polecenie generuje token SAS z pełnymi uprawnieniami dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="f95e9-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="f95e9-115">Polecenie ogranicza token do zakresu określonego przez parametry *StartPartitionKey* i *EndPartitionKey* .</span><span class="sxs-lookup"><span data-stu-id="f95e9-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="f95e9-116">Przykład 3: generowanie tokenu SAS z zapisanymi zasadami dostępu dla tabeli</span><span class="sxs-lookup"><span data-stu-id="f95e9-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="f95e9-117">To polecenie generuje token SAS dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="f95e9-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="f95e9-118">Polecenie określa zapisane zasady dostępu o nazwie ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="f95e9-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="f95e9-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f95e9-119">PARAMETERS</span></span>

### <span data-ttu-id="f95e9-120">-Context</span><span class="sxs-lookup"><span data-stu-id="f95e9-120">-Context</span></span>
<span data-ttu-id="f95e9-121">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f95e9-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f95e9-122">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f95e9-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f95e9-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="f95e9-123">-EndPartitionKey</span></span>
<span data-ttu-id="f95e9-124">Określa klucz partycji końca zakresu dla tokenu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f95e9-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95e9-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="f95e9-125">-EndRowKey</span></span>
<span data-ttu-id="f95e9-126">Określa klucz wiersza dla końca zakresu dla tokenu, który jest tworzony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f95e9-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95e9-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f95e9-127">-ExpiryTime</span></span>
<span data-ttu-id="f95e9-128">Określa, kiedy wygasa token SAS.</span><span class="sxs-lookup"><span data-stu-id="f95e9-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="f95e9-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="f95e9-129">-FullUri</span></span>
<span data-ttu-id="f95e9-130">Wskazuje, że to polecenie cmdlet zwraca identyfikator URI pełnej kolejki z tokenem SAS.</span><span class="sxs-lookup"><span data-stu-id="f95e9-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="f95e9-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f95e9-131">-IPAddressOrRange</span></span>
<span data-ttu-id="f95e9-132">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="f95e9-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="f95e9-133">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="f95e9-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="f95e9-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f95e9-134">-Name</span></span>
<span data-ttu-id="f95e9-135">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f95e9-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="f95e9-136">To polecenie cmdlet tworzy token SAS dla tabeli, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f95e9-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f95e9-137">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="f95e9-137">-Permission</span></span>
<span data-ttu-id="f95e9-138">Określa uprawnienia dotyczące tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f95e9-138">Specifies permissions for an Azure Storage table.</span></span>

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

### <span data-ttu-id="f95e9-139">-Policy</span><span class="sxs-lookup"><span data-stu-id="f95e9-139">-Policy</span></span>
<span data-ttu-id="f95e9-140">Określa zapisane zasady dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="f95e9-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="f95e9-141">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="f95e9-141">-Protocol</span></span>
<span data-ttu-id="f95e9-142">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="f95e9-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="f95e9-143">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f95e9-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="f95e9-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f95e9-144">HttpsOnly</span></span>
* <span data-ttu-id="f95e9-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="f95e9-145">HttpsOrHttp</span></span>

<span data-ttu-id="f95e9-146">Wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="f95e9-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="f95e9-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="f95e9-147">-StartPartitionKey</span></span>
<span data-ttu-id="f95e9-148">Określa klucz partycji początku zakresu dla tokenu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f95e9-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95e9-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="f95e9-149">-StartRowKey</span></span>
<span data-ttu-id="f95e9-150">Określa klucz wiersza początku zakresu dla tokenu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f95e9-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95e9-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f95e9-151">-StartTime</span></span>
<span data-ttu-id="f95e9-152">Określa, kiedy token SAS stanie się ważny.</span><span class="sxs-lookup"><span data-stu-id="f95e9-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="f95e9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95e9-153">CommonParameters</span></span>
<span data-ttu-id="f95e9-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f95e9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95e9-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f95e9-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95e9-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f95e9-156">INPUTS</span></span>

### <span data-ttu-id="f95e9-157">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f95e9-157">IStorageContext</span></span>

<span data-ttu-id="f95e9-158">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="f95e9-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="f95e9-159">Ciąg</span><span class="sxs-lookup"><span data-stu-id="f95e9-159">String</span></span>

<span data-ttu-id="f95e9-160">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="f95e9-160">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f95e9-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f95e9-161">OUTPUTS</span></span>

### <span data-ttu-id="f95e9-162">System. String</span><span class="sxs-lookup"><span data-stu-id="f95e9-162">System.String</span></span>

## <span data-ttu-id="f95e9-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f95e9-163">NOTES</span></span>

## <span data-ttu-id="f95e9-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f95e9-164">RELATED LINKS</span></span>

[<span data-ttu-id="f95e9-165">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f95e9-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
