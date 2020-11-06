---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac818fd403df9b159671f5889e068bda82a086d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523665"
---
# <span data-ttu-id="14daa-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="14daa-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="14daa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14daa-102">SYNOPSIS</span></span>
<span data-ttu-id="14daa-103">Generuje token podpisu dostępu współdzielonego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="14daa-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="14daa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14daa-104">SYNTAX</span></span>

### <span data-ttu-id="14daa-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="14daa-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="14daa-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="14daa-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="14daa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="14daa-107">DESCRIPTION</span></span>
<span data-ttu-id="14daa-108">Polecenie cmdlet **New-AzureStorageQueueSASToken** generuje token podpisu dostępu współdzielonego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="14daa-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="14daa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14daa-109">EXAMPLES</span></span>

### <span data-ttu-id="14daa-110">Przykład 1. Generuj token SAS kolejki z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="14daa-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="14daa-111">W tym przykładzie Wygenerowano token SAS kolejki z pełnymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="14daa-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="14daa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14daa-112">PARAMETERS</span></span>

### <span data-ttu-id="14daa-113">-Context</span><span class="sxs-lookup"><span data-stu-id="14daa-113">-Context</span></span>
<span data-ttu-id="14daa-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="14daa-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="14daa-115">Możesz je utworzyć, New-AzureStorageContext polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14daa-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="14daa-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="14daa-116">-ExpiryTime</span></span>
<span data-ttu-id="14daa-117">Określa, kiedy podpis udostępnionej dostępu nie jest już ważny.</span><span class="sxs-lookup"><span data-stu-id="14daa-117">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="14daa-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="14daa-118">-FullUri</span></span>
<span data-ttu-id="14daa-119">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="14daa-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="14daa-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="14daa-120">-IPAddressOrRange</span></span>
<span data-ttu-id="14daa-121">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="14daa-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="14daa-122">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="14daa-122">The range is inclusive.</span></span>

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

### <span data-ttu-id="14daa-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14daa-123">-Name</span></span>
<span data-ttu-id="14daa-124">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="14daa-124">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="14daa-125">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="14daa-125">-Permission</span></span>
<span data-ttu-id="14daa-126">Określa uprawnienia do kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="14daa-126">Specifies permissions for a storage queue.</span></span>

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

### <span data-ttu-id="14daa-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="14daa-127">-Policy</span></span>
<span data-ttu-id="14daa-128">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="14daa-128">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="14daa-129">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="14daa-129">-Protocol</span></span>
<span data-ttu-id="14daa-130">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="14daa-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="14daa-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="14daa-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="14daa-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="14daa-132">HttpsOnly</span></span>
* <span data-ttu-id="14daa-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="14daa-133">HttpsOrHttp</span></span>

<span data-ttu-id="14daa-134">Wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="14daa-134">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="14daa-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="14daa-135">-StartTime</span></span>
<span data-ttu-id="14daa-136">Określa, czy podpis udostępniony jest prawidłowy.</span><span class="sxs-lookup"><span data-stu-id="14daa-136">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="14daa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14daa-137">CommonParameters</span></span>
<span data-ttu-id="14daa-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14daa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14daa-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14daa-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14daa-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14daa-140">INPUTS</span></span>

## <span data-ttu-id="14daa-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14daa-141">OUTPUTS</span></span>

## <span data-ttu-id="14daa-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14daa-142">NOTES</span></span>

## <span data-ttu-id="14daa-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14daa-143">RELATED LINKS</span></span>

