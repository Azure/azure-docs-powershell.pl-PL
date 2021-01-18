---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 17a7e32d0686e68b70f2129edfbb617661057218
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502729"
---
# <span data-ttu-id="98dcc-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="98dcc-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="98dcc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="98dcc-103">Generuje token podpisu dostępu współdzielonego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98dcc-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="98dcc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98dcc-104">SYNTAX</span></span>

### <span data-ttu-id="98dcc-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="98dcc-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98dcc-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="98dcc-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98dcc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98dcc-107">DESCRIPTION</span></span>
<span data-ttu-id="98dcc-108">Polecenie cmdlet **New-AzStorageQueueSASToken** generuje token podpisu dostępu współdzielonego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98dcc-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="98dcc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98dcc-109">EXAMPLES</span></span>

### <span data-ttu-id="98dcc-110">Przykład 1. Generuj token SAS kolejki z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="98dcc-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="98dcc-111">W tym przykładzie Wygenerowano token SAS kolejki z pełnymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="98dcc-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="98dcc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98dcc-112">PARAMETERS</span></span>

### <span data-ttu-id="98dcc-113">-Context</span><span class="sxs-lookup"><span data-stu-id="98dcc-113">-Context</span></span>
<span data-ttu-id="98dcc-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="98dcc-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="98dcc-115">Możesz je utworzyć, New-AzStorageContext polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98dcc-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="98dcc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98dcc-116">-DefaultProfile</span></span>
<span data-ttu-id="98dcc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98dcc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98dcc-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="98dcc-118">-ExpiryTime</span></span>
<span data-ttu-id="98dcc-119">Określa, kiedy podpis udostępnionej dostępu nie jest już ważny.</span><span class="sxs-lookup"><span data-stu-id="98dcc-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="98dcc-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="98dcc-120">-FullUri</span></span>
<span data-ttu-id="98dcc-121">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="98dcc-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="98dcc-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="98dcc-122">-IPAddressOrRange</span></span>
<span data-ttu-id="98dcc-123">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="98dcc-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="98dcc-124">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="98dcc-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="98dcc-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98dcc-125">-Name</span></span>
<span data-ttu-id="98dcc-126">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98dcc-126">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="98dcc-127">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="98dcc-127">-Permission</span></span>
<span data-ttu-id="98dcc-128">Określa uprawnienia do kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="98dcc-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="98dcc-129">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="98dcc-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="98dcc-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="98dcc-130">-Policy</span></span>
<span data-ttu-id="98dcc-131">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="98dcc-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="98dcc-132">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="98dcc-132">-Protocol</span></span>
<span data-ttu-id="98dcc-133">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="98dcc-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="98dcc-134">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="98dcc-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="98dcc-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="98dcc-135">HttpsOnly</span></span>
* <span data-ttu-id="98dcc-136">HttpsOrHttp wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="98dcc-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="98dcc-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="98dcc-137">-StartTime</span></span>
<span data-ttu-id="98dcc-138">Określa, czy podpis udostępniony jest prawidłowy.</span><span class="sxs-lookup"><span data-stu-id="98dcc-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="98dcc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98dcc-139">CommonParameters</span></span>
<span data-ttu-id="98dcc-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98dcc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98dcc-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98dcc-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98dcc-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98dcc-142">INPUTS</span></span>

### <span data-ttu-id="98dcc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="98dcc-143">System.String</span></span>

### <span data-ttu-id="98dcc-144">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="98dcc-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="98dcc-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98dcc-145">OUTPUTS</span></span>

### <span data-ttu-id="98dcc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="98dcc-146">System.String</span></span>

## <span data-ttu-id="98dcc-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98dcc-147">NOTES</span></span>

## <span data-ttu-id="98dcc-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98dcc-148">RELATED LINKS</span></span>
