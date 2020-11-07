---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: 190db8ff50c3c52fb8d43a2cdbd509f9e67ea63b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892122"
---
# <span data-ttu-id="90848-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="90848-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="90848-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90848-102">SYNOPSIS</span></span>
<span data-ttu-id="90848-103">Generuje token SAS dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="90848-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="90848-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90848-104">SYNTAX</span></span>

### <span data-ttu-id="90848-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="90848-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90848-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="90848-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90848-107">Opis</span><span class="sxs-lookup"><span data-stu-id="90848-107">DESCRIPTION</span></span>
<span data-ttu-id="90848-108">Polecenie cmdlet **New-AzStorageTableSASToken** generuje token dostępu współużytkowanego (SAS) dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="90848-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="90848-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90848-109">EXAMPLES</span></span>

### <span data-ttu-id="90848-110">Przykład 1. Generuj token SAS z pełnymi uprawnieniami dla tabeli</span><span class="sxs-lookup"><span data-stu-id="90848-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="90848-111">To polecenie generuje token SAS z pełnymi uprawnieniami dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="90848-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="90848-112">Token ten jest przeznaczony dla uprawnień Odczyt, Dodawanie, aktualizowanie i usuwanie.</span><span class="sxs-lookup"><span data-stu-id="90848-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="90848-113">Przykład 2: generowanie tokenu SAS dla zakresu partycji</span><span class="sxs-lookup"><span data-stu-id="90848-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="90848-114">To polecenie generuje token SAS z pełnymi uprawnieniami dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="90848-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="90848-115">Polecenie ogranicza token do zakresu określonego przez parametry *StartPartitionKey* i *EndPartitionKey* .</span><span class="sxs-lookup"><span data-stu-id="90848-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="90848-116">Przykład 3: generowanie tokenu SAS z zapisanymi zasadami dostępu dla tabeli</span><span class="sxs-lookup"><span data-stu-id="90848-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="90848-117">To polecenie generuje token SAS dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="90848-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="90848-118">Polecenie określa zapisane zasady dostępu o nazwie ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="90848-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="90848-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90848-119">PARAMETERS</span></span>

### <span data-ttu-id="90848-120">-Context</span><span class="sxs-lookup"><span data-stu-id="90848-120">-Context</span></span>
<span data-ttu-id="90848-121">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="90848-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="90848-122">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="90848-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="90848-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90848-123">-DefaultProfile</span></span>
<span data-ttu-id="90848-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90848-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90848-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="90848-125">-EndPartitionKey</span></span>
<span data-ttu-id="90848-126">Określa klucz partycji końca zakresu dla tokenu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90848-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="90848-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="90848-127">-EndRowKey</span></span>
<span data-ttu-id="90848-128">Określa klucz wiersza dla końca zakresu dla tokenu, który jest tworzony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90848-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="90848-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="90848-129">-ExpiryTime</span></span>
<span data-ttu-id="90848-130">Określa, kiedy wygasa token SAS.</span><span class="sxs-lookup"><span data-stu-id="90848-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="90848-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="90848-131">-FullUri</span></span>
<span data-ttu-id="90848-132">Wskazuje, że to polecenie cmdlet zwraca identyfikator URI pełnej kolejki z tokenem SAS.</span><span class="sxs-lookup"><span data-stu-id="90848-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="90848-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="90848-133">-IPAddressOrRange</span></span>
<span data-ttu-id="90848-134">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="90848-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="90848-135">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="90848-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="90848-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90848-136">-Name</span></span>
<span data-ttu-id="90848-137">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="90848-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="90848-138">To polecenie cmdlet tworzy token SAS dla tabeli, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="90848-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="90848-139">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="90848-139">-Permission</span></span>
<span data-ttu-id="90848-140">Określa uprawnienia dotyczące tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="90848-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="90848-141">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="90848-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="90848-142">-Policy</span><span class="sxs-lookup"><span data-stu-id="90848-142">-Policy</span></span>
<span data-ttu-id="90848-143">Określa zapisane zasady dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="90848-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="90848-144">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="90848-144">-Protocol</span></span>
<span data-ttu-id="90848-145">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="90848-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="90848-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="90848-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="90848-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="90848-147">HttpsOnly</span></span>
* <span data-ttu-id="90848-148">HttpsOrHttp wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="90848-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAz.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90848-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="90848-149">-StartPartitionKey</span></span>
<span data-ttu-id="90848-150">Określa klucz partycji początku zakresu dla tokenu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90848-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="90848-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="90848-151">-StartRowKey</span></span>
<span data-ttu-id="90848-152">Określa klucz wiersza początku zakresu dla tokenu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90848-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="90848-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="90848-153">-StartTime</span></span>
<span data-ttu-id="90848-154">Określa, kiedy token SAS stanie się ważny.</span><span class="sxs-lookup"><span data-stu-id="90848-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="90848-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90848-155">CommonParameters</span></span>
<span data-ttu-id="90848-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90848-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90848-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90848-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90848-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90848-158">INPUTS</span></span>

### <span data-ttu-id="90848-159">System. String</span><span class="sxs-lookup"><span data-stu-id="90848-159">System.String</span></span>

### <span data-ttu-id="90848-160">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="90848-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="90848-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90848-161">OUTPUTS</span></span>

### <span data-ttu-id="90848-162">System. String</span><span class="sxs-lookup"><span data-stu-id="90848-162">System.String</span></span>

## <span data-ttu-id="90848-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90848-163">NOTES</span></span>

## <span data-ttu-id="90848-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90848-164">RELATED LINKS</span></span>

[<span data-ttu-id="90848-165">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="90848-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
