---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 904305e383803e8ef672a82689794296f7c9b84d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554249"
---
# <span data-ttu-id="43858-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="43858-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="43858-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43858-102">SYNOPSIS</span></span>
<span data-ttu-id="43858-103">Generuje token podpisu dostępu współdzielonego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43858-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43858-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43858-104">SYNTAX</span></span>

### <span data-ttu-id="43858-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="43858-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="43858-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="43858-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="43858-107">Opis</span><span class="sxs-lookup"><span data-stu-id="43858-107">DESCRIPTION</span></span>
<span data-ttu-id="43858-108">Polecenie cmdlet **New-AzureStorageQueueSASToken** generuje token podpisu dostępu współdzielonego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43858-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="43858-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43858-109">EXAMPLES</span></span>

### <span data-ttu-id="43858-110">Przykład 1. Generuj token SAS kolejki z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="43858-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="43858-111">W tym przykładzie Wygenerowano token SAS kolejki z pełnymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="43858-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="43858-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43858-112">PARAMETERS</span></span>

### <span data-ttu-id="43858-113">-Context</span><span class="sxs-lookup"><span data-stu-id="43858-113">-Context</span></span>
<span data-ttu-id="43858-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="43858-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="43858-115">Możesz je utworzyć, New-AzureStorageContext polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43858-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="43858-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="43858-116">-ExpiryTime</span></span>
<span data-ttu-id="43858-117">Określa, kiedy podpis udostępnionej dostępu nie jest już ważny.</span><span class="sxs-lookup"><span data-stu-id="43858-117">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="43858-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="43858-118">-FullUri</span></span>
<span data-ttu-id="43858-119">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="43858-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="43858-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="43858-120">-IPAddressOrRange</span></span>
<span data-ttu-id="43858-121">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="43858-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="43858-122">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="43858-122">The range is inclusive.</span></span>

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

### <span data-ttu-id="43858-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43858-123">-Name</span></span>
<span data-ttu-id="43858-124">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43858-124">Specifies an Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43858-125">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="43858-125">-Permission</span></span>
<span data-ttu-id="43858-126">Określa uprawnienia do kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="43858-126">Specifies permissions for a storage queue.</span></span>

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

### <span data-ttu-id="43858-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="43858-127">-Policy</span></span>
<span data-ttu-id="43858-128">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="43858-128">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="43858-129">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="43858-129">-Protocol</span></span>
<span data-ttu-id="43858-130">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="43858-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="43858-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="43858-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="43858-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="43858-132">HttpsOnly</span></span>
* <span data-ttu-id="43858-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="43858-133">HttpsOrHttp</span></span>

<span data-ttu-id="43858-134">Wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="43858-134">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="43858-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="43858-135">-StartTime</span></span>
<span data-ttu-id="43858-136">Określa, czy podpis udostępniony jest prawidłowy.</span><span class="sxs-lookup"><span data-stu-id="43858-136">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="43858-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43858-137">CommonParameters</span></span>
<span data-ttu-id="43858-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43858-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43858-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43858-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43858-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43858-140">INPUTS</span></span>

### <span data-ttu-id="43858-141">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="43858-141">IStorageContext</span></span>

<span data-ttu-id="43858-142">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="43858-142">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="43858-143">Ciąg</span><span class="sxs-lookup"><span data-stu-id="43858-143">String</span></span>

<span data-ttu-id="43858-144">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="43858-144">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="43858-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43858-145">OUTPUTS</span></span>

### <span data-ttu-id="43858-146">System. String</span><span class="sxs-lookup"><span data-stu-id="43858-146">System.String</span></span>

## <span data-ttu-id="43858-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43858-147">NOTES</span></span>

## <span data-ttu-id="43858-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43858-148">RELATED LINKS</span></span>

