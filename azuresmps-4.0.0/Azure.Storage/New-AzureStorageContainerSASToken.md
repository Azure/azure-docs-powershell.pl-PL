---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: ''
schema: 2.0.0
ms.openlocfilehash: becdf63590b5c5abc5e7095b96e13586232311d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523985"
---
# <span data-ttu-id="770a1-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="770a1-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="770a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="770a1-102">SYNOPSIS</span></span>
<span data-ttu-id="770a1-103">Generuje token SAS dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="770a1-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="770a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="770a1-104">SYNTAX</span></span>

### <span data-ttu-id="770a1-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="770a1-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="770a1-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="770a1-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="770a1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="770a1-107">DESCRIPTION</span></span>
<span data-ttu-id="770a1-108">Polecenie cmdlet **New-AzureStorageContainerSASToken** generuje token dostępu współużytkowanego (SAS) dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="770a1-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="770a1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="770a1-109">EXAMPLES</span></span>

### <span data-ttu-id="770a1-110">Przykład 1. Generuj token SAS kontenera z uprawnieniem pełny kontener</span><span class="sxs-lookup"><span data-stu-id="770a1-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="770a1-111">W tym przykładzie Wygenerowano token SAS kontenera z uprawnieniem pełnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="770a1-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="770a1-112">Przykład 2: generowanie wielu tokenów SAS kontenera według rurociągu</span><span class="sxs-lookup"><span data-stu-id="770a1-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="770a1-113">W tym przykładzie Wygenerowano wiele tokenów SAS kontenera za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="770a1-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="770a1-114">Przykład 3: generowanie tokenu SAS kontenera z zasadami dostępu współużytkowanego</span><span class="sxs-lookup"><span data-stu-id="770a1-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="770a1-115">W tym przykładzie Wygenerowano token SAS kontenera z zasadami dostępu współużytkowanego.</span><span class="sxs-lookup"><span data-stu-id="770a1-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="770a1-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="770a1-116">PARAMETERS</span></span>

### <span data-ttu-id="770a1-117">-Context</span><span class="sxs-lookup"><span data-stu-id="770a1-117">-Context</span></span>
<span data-ttu-id="770a1-118">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="770a1-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="770a1-119">Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="770a1-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="770a1-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="770a1-120">-ExpiryTime</span></span>
<span data-ttu-id="770a1-121">Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="770a1-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="770a1-122">Jeśli użytkownik ustawi czas rozpoczęcia, ale nie czas wygaśnięcia, czas wygaśnięcia jest ustawiany na czas rozpoczęcia Plus o godzinę.</span><span class="sxs-lookup"><span data-stu-id="770a1-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="770a1-123">Jeśli nie określono godziny rozpoczęcia ani godziny wygaśnięcia, czas wygaśnięcia jest ustawiany na bieżący czas plus co godzinę.</span><span class="sxs-lookup"><span data-stu-id="770a1-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="770a1-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="770a1-124">-FullUri</span></span>
<span data-ttu-id="770a1-125">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="770a1-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="770a1-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="770a1-126">-IPAddressOrRange</span></span>
<span data-ttu-id="770a1-127">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="770a1-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="770a1-128">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="770a1-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="770a1-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="770a1-129">-Name</span></span>
<span data-ttu-id="770a1-130">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="770a1-130">Specifies an Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="770a1-131">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="770a1-131">-Permission</span></span>
<span data-ttu-id="770a1-132">Określa uprawnienia kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="770a1-132">Specifies permissions for a storage container.</span></span>

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

### <span data-ttu-id="770a1-133">-Policy</span><span class="sxs-lookup"><span data-stu-id="770a1-133">-Policy</span></span>
<span data-ttu-id="770a1-134">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="770a1-134">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="770a1-135">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="770a1-135">-Protocol</span></span>
<span data-ttu-id="770a1-136">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="770a1-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="770a1-137">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="770a1-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="770a1-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="770a1-138">HttpsOnly</span></span>
* <span data-ttu-id="770a1-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="770a1-139">HttpsOrHttp</span></span>

<span data-ttu-id="770a1-140">Wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="770a1-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="770a1-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="770a1-141">-StartTime</span></span>
<span data-ttu-id="770a1-142">Określa czas, po upływie którego podpis udostępniony będzie ważny.</span><span class="sxs-lookup"><span data-stu-id="770a1-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="770a1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770a1-143">CommonParameters</span></span>
<span data-ttu-id="770a1-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770a1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770a1-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="770a1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770a1-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="770a1-146">INPUTS</span></span>

## <span data-ttu-id="770a1-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="770a1-147">OUTPUTS</span></span>

## <span data-ttu-id="770a1-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="770a1-148">NOTES</span></span>

## <span data-ttu-id="770a1-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="770a1-149">RELATED LINKS</span></span>

[<span data-ttu-id="770a1-150">Nowe — AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="770a1-150">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
