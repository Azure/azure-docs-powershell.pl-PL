---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablesastoken
schema: 2.0.0
ms.openlocfilehash: 29c5cf9b48126d4b8544cf80ad6fa78acc51ae93
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899410"
---
# <span data-ttu-id="c2e85-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="c2e85-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="c2e85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2e85-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e85-103">Generuje token SAS dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2e85-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2e85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2e85-104">SYNTAX</span></span>

### <span data-ttu-id="c2e85-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="c2e85-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2e85-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="c2e85-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2e85-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c2e85-107">DESCRIPTION</span></span>
<span data-ttu-id="c2e85-108">Polecenie cmdlet **New-AzureStorageTableSASToken** generuje token dostępu współużytkowanego (SAS) dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2e85-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="c2e85-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2e85-109">EXAMPLES</span></span>

### <span data-ttu-id="c2e85-110">Przykład 1. Generuj token SAS z pełnymi uprawnieniami dla tabeli</span><span class="sxs-lookup"><span data-stu-id="c2e85-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="c2e85-111">To polecenie generuje token SAS z pełnymi uprawnieniami dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="c2e85-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="c2e85-112">Token ten jest przeznaczony dla uprawnień Odczyt, Dodawanie, aktualizowanie i usuwanie.</span><span class="sxs-lookup"><span data-stu-id="c2e85-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="c2e85-113">Przykład 2: generowanie tokenu SAS dla zakresu partycji</span><span class="sxs-lookup"><span data-stu-id="c2e85-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="c2e85-114">To polecenie generuje token SAS z pełnymi uprawnieniami dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="c2e85-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="c2e85-115">Polecenie ogranicza token do zakresu określonego przez parametry *StartPartitionKey* i *EndPartitionKey* .</span><span class="sxs-lookup"><span data-stu-id="c2e85-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="c2e85-116">Przykład 3: generowanie tokenu SAS z zapisanymi zasadami dostępu dla tabeli</span><span class="sxs-lookup"><span data-stu-id="c2e85-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="c2e85-117">To polecenie generuje token SAS dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="c2e85-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="c2e85-118">Polecenie określa zapisane zasady dostępu o nazwie ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="c2e85-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="c2e85-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2e85-119">PARAMETERS</span></span>

### <span data-ttu-id="c2e85-120">-Context</span><span class="sxs-lookup"><span data-stu-id="c2e85-120">-Context</span></span>
<span data-ttu-id="c2e85-121">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c2e85-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c2e85-122">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c2e85-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c2e85-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e85-123">-DefaultProfile</span></span>
<span data-ttu-id="c2e85-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2e85-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2e85-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="c2e85-125">-EndPartitionKey</span></span>
<span data-ttu-id="c2e85-126">Określa klucz partycji końca zakresu dla tokenu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e85-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e85-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="c2e85-127">-EndRowKey</span></span>
<span data-ttu-id="c2e85-128">Określa klucz wiersza dla końca zakresu dla tokenu, który jest tworzony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e85-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e85-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c2e85-129">-ExpiryTime</span></span>
<span data-ttu-id="c2e85-130">Określa, kiedy wygasa token SAS.</span><span class="sxs-lookup"><span data-stu-id="c2e85-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="c2e85-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="c2e85-131">-FullUri</span></span>
<span data-ttu-id="c2e85-132">Wskazuje, że to polecenie cmdlet zwraca identyfikator URI pełnej kolejki z tokenem SAS.</span><span class="sxs-lookup"><span data-stu-id="c2e85-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="c2e85-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c2e85-133">-IPAddressOrRange</span></span>
<span data-ttu-id="c2e85-134">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="c2e85-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c2e85-135">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="c2e85-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="c2e85-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2e85-136">-Name</span></span>
<span data-ttu-id="c2e85-137">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2e85-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="c2e85-138">To polecenie cmdlet tworzy token SAS dla tabeli, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c2e85-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2e85-139">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="c2e85-139">-Permission</span></span>
<span data-ttu-id="c2e85-140">Określa uprawnienia dotyczące tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2e85-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="c2e85-141">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="c2e85-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="c2e85-142">-Policy</span><span class="sxs-lookup"><span data-stu-id="c2e85-142">-Policy</span></span>
<span data-ttu-id="c2e85-143">Określa zapisane zasady dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="c2e85-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="c2e85-144">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="c2e85-144">-Protocol</span></span>
<span data-ttu-id="c2e85-145">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="c2e85-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="c2e85-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c2e85-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="c2e85-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c2e85-147">HttpsOnly</span></span>
* <span data-ttu-id="c2e85-148">HttpsOrHttp wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="c2e85-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="c2e85-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="c2e85-149">-StartPartitionKey</span></span>
<span data-ttu-id="c2e85-150">Określa klucz partycji początku zakresu dla tokenu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e85-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e85-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="c2e85-151">-StartRowKey</span></span>
<span data-ttu-id="c2e85-152">Określa klucz wiersza początku zakresu dla tokenu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e85-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e85-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c2e85-153">-StartTime</span></span>
<span data-ttu-id="c2e85-154">Określa, kiedy token SAS stanie się ważny.</span><span class="sxs-lookup"><span data-stu-id="c2e85-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="c2e85-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e85-155">CommonParameters</span></span>
<span data-ttu-id="c2e85-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2e85-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e85-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2e85-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e85-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2e85-158">INPUTS</span></span>

### <span data-ttu-id="c2e85-159">System. String</span><span class="sxs-lookup"><span data-stu-id="c2e85-159">System.String</span></span>

### <span data-ttu-id="c2e85-160">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c2e85-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c2e85-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2e85-161">OUTPUTS</span></span>

### <span data-ttu-id="c2e85-162">System. String</span><span class="sxs-lookup"><span data-stu-id="c2e85-162">System.String</span></span>

## <span data-ttu-id="c2e85-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2e85-163">NOTES</span></span>

## <span data-ttu-id="c2e85-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2e85-164">RELATED LINKS</span></span>

[<span data-ttu-id="c2e85-165">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c2e85-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
