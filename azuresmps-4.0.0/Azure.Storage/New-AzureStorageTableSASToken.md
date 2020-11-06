---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39870fe9fe9ac4223bccf15908c960db29d25252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524189"
---
# <span data-ttu-id="38f07-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="38f07-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="38f07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38f07-102">SYNOPSIS</span></span>
<span data-ttu-id="38f07-103">Generuje token SAS dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38f07-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="38f07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38f07-104">SYNTAX</span></span>

### <span data-ttu-id="38f07-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="38f07-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="38f07-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="38f07-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="38f07-107">Opis</span><span class="sxs-lookup"><span data-stu-id="38f07-107">DESCRIPTION</span></span>
<span data-ttu-id="38f07-108">Polecenie cmdlet **New-AzureStorageTableSASToken** generuje token dostępu współużytkowanego (SAS) dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38f07-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="38f07-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38f07-109">EXAMPLES</span></span>

### <span data-ttu-id="38f07-110">Przykład 1. Generuj token SAS z pełnymi uprawnieniami dla tabeli</span><span class="sxs-lookup"><span data-stu-id="38f07-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="38f07-111">To polecenie generuje token SAS z pełnymi uprawnieniami dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="38f07-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="38f07-112">Token ten jest przeznaczony dla uprawnień Odczyt, Dodawanie, aktualizowanie i usuwanie.</span><span class="sxs-lookup"><span data-stu-id="38f07-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="38f07-113">Przykład 2: generowanie tokenu SAS dla zakresu partycji</span><span class="sxs-lookup"><span data-stu-id="38f07-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="38f07-114">To polecenie generuje token SAS z pełnymi uprawnieniami dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="38f07-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="38f07-115">Polecenie ogranicza token do zakresu określonego przez parametry *StartPartitionKey* i *EndPartitionKey* .</span><span class="sxs-lookup"><span data-stu-id="38f07-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="38f07-116">Przykład 3: generowanie tokenu SAS z zapisanymi zasadami dostępu dla tabeli</span><span class="sxs-lookup"><span data-stu-id="38f07-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="38f07-117">To polecenie generuje token SAS dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="38f07-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="38f07-118">Polecenie określa zapisane zasady dostępu o nazwie ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="38f07-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="38f07-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38f07-119">PARAMETERS</span></span>

### <span data-ttu-id="38f07-120">-Context</span><span class="sxs-lookup"><span data-stu-id="38f07-120">-Context</span></span>
<span data-ttu-id="38f07-121">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="38f07-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="38f07-122">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="38f07-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="38f07-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="38f07-123">-EndPartitionKey</span></span>
<span data-ttu-id="38f07-124">Określa klucz partycji końca zakresu dla tokenu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38f07-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="38f07-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="38f07-125">-EndRowKey</span></span>
<span data-ttu-id="38f07-126">Określa klucz wiersza dla końca zakresu dla tokenu, który jest tworzony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38f07-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="38f07-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="38f07-127">-ExpiryTime</span></span>
<span data-ttu-id="38f07-128">Określa, kiedy wygasa token SAS.</span><span class="sxs-lookup"><span data-stu-id="38f07-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="38f07-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="38f07-129">-FullUri</span></span>
<span data-ttu-id="38f07-130">Wskazuje, że to polecenie cmdlet zwraca identyfikator URI pełnej kolejki z tokenem SAS.</span><span class="sxs-lookup"><span data-stu-id="38f07-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="38f07-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="38f07-131">-IPAddressOrRange</span></span>
<span data-ttu-id="38f07-132">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="38f07-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="38f07-133">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="38f07-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="38f07-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="38f07-134">-Name</span></span>
<span data-ttu-id="38f07-135">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38f07-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="38f07-136">To polecenie cmdlet tworzy token SAS dla tabeli, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="38f07-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="38f07-137">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="38f07-137">-Permission</span></span>
<span data-ttu-id="38f07-138">Określa uprawnienia dotyczące tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38f07-138">Specifies permissions for an Azure Storage table.</span></span>

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

### <span data-ttu-id="38f07-139">-Policy</span><span class="sxs-lookup"><span data-stu-id="38f07-139">-Policy</span></span>
<span data-ttu-id="38f07-140">Określa zapisane zasady dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="38f07-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="38f07-141">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="38f07-141">-Protocol</span></span>
<span data-ttu-id="38f07-142">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="38f07-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="38f07-143">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="38f07-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="38f07-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="38f07-144">HttpsOnly</span></span>
* <span data-ttu-id="38f07-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="38f07-145">HttpsOrHttp</span></span>

<span data-ttu-id="38f07-146">Wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="38f07-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="38f07-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="38f07-147">-StartPartitionKey</span></span>
<span data-ttu-id="38f07-148">Określa klucz partycji początku zakresu dla tokenu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38f07-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="38f07-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="38f07-149">-StartRowKey</span></span>
<span data-ttu-id="38f07-150">Określa klucz wiersza początku zakresu dla tokenu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38f07-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="38f07-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="38f07-151">-StartTime</span></span>
<span data-ttu-id="38f07-152">Określa, kiedy token SAS stanie się ważny.</span><span class="sxs-lookup"><span data-stu-id="38f07-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="38f07-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f07-153">CommonParameters</span></span>
<span data-ttu-id="38f07-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f07-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f07-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f07-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f07-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38f07-156">INPUTS</span></span>

## <span data-ttu-id="38f07-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38f07-157">OUTPUTS</span></span>

## <span data-ttu-id="38f07-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38f07-158">NOTES</span></span>

## <span data-ttu-id="38f07-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38f07-159">RELATED LINKS</span></span>

[<span data-ttu-id="38f07-160">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="38f07-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
