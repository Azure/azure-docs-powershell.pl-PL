---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuesastoken
schema: 2.0.0
ms.openlocfilehash: b002f518d63fb3ed4ed34d007f72b57e4db41ae5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898824"
---
# <span data-ttu-id="53d4f-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="53d4f-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="53d4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="53d4f-103">Generuje token podpisu dostępu współdzielonego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53d4f-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53d4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53d4f-104">SYNTAX</span></span>

### <span data-ttu-id="53d4f-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="53d4f-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53d4f-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="53d4f-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53d4f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="53d4f-107">DESCRIPTION</span></span>
<span data-ttu-id="53d4f-108">Polecenie cmdlet **New-AzureStorageQueueSASToken** generuje token podpisu dostępu współdzielonego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53d4f-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="53d4f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53d4f-109">EXAMPLES</span></span>

### <span data-ttu-id="53d4f-110">Przykład 1. Generuj token SAS kolejki z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="53d4f-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="53d4f-111">W tym przykładzie Wygenerowano token SAS kolejki z pełnymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="53d4f-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="53d4f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53d4f-112">PARAMETERS</span></span>

### <span data-ttu-id="53d4f-113">-Context</span><span class="sxs-lookup"><span data-stu-id="53d4f-113">-Context</span></span>
<span data-ttu-id="53d4f-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="53d4f-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="53d4f-115">Możesz je utworzyć, New-AzureStorageContext polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53d4f-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="53d4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53d4f-116">-DefaultProfile</span></span>
<span data-ttu-id="53d4f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53d4f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53d4f-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="53d4f-118">-ExpiryTime</span></span>
<span data-ttu-id="53d4f-119">Określa, kiedy podpis udostępnionej dostępu nie jest już ważny.</span><span class="sxs-lookup"><span data-stu-id="53d4f-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="53d4f-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="53d4f-120">-FullUri</span></span>
<span data-ttu-id="53d4f-121">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="53d4f-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="53d4f-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="53d4f-122">-IPAddressOrRange</span></span>
<span data-ttu-id="53d4f-123">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="53d4f-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="53d4f-124">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="53d4f-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="53d4f-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53d4f-125">-Name</span></span>
<span data-ttu-id="53d4f-126">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53d4f-126">Specifies an Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53d4f-127">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="53d4f-127">-Permission</span></span>
<span data-ttu-id="53d4f-128">Określa uprawnienia do kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="53d4f-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="53d4f-129">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="53d4f-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="53d4f-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="53d4f-130">-Policy</span></span>
<span data-ttu-id="53d4f-131">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="53d4f-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="53d4f-132">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="53d4f-132">-Protocol</span></span>
<span data-ttu-id="53d4f-133">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="53d4f-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="53d4f-134">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="53d4f-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="53d4f-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="53d4f-135">HttpsOnly</span></span>
* <span data-ttu-id="53d4f-136">HttpsOrHttp wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="53d4f-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="53d4f-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="53d4f-137">-StartTime</span></span>
<span data-ttu-id="53d4f-138">Określa, czy podpis udostępniony jest prawidłowy.</span><span class="sxs-lookup"><span data-stu-id="53d4f-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="53d4f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53d4f-139">CommonParameters</span></span>
<span data-ttu-id="53d4f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53d4f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53d4f-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53d4f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53d4f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53d4f-142">INPUTS</span></span>

### <span data-ttu-id="53d4f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="53d4f-143">System.String</span></span>

### <span data-ttu-id="53d4f-144">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="53d4f-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="53d4f-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53d4f-145">OUTPUTS</span></span>

### <span data-ttu-id="53d4f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="53d4f-146">System.String</span></span>

## <span data-ttu-id="53d4f-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53d4f-147">NOTES</span></span>

## <span data-ttu-id="53d4f-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53d4f-148">RELATED LINKS</span></span>
