---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 3ecea2e4eece9b4e0161a90cc597218d04a29bfc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002401"
---
# <span data-ttu-id="5f605-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="5f605-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="5f605-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f605-102">SYNOPSIS</span></span>
<span data-ttu-id="5f605-103">Generuje token podpisu dostępu udostępnionego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f605-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="5f605-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5f605-104">SYNTAX</span></span>

### <span data-ttu-id="5f605-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="5f605-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f605-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="5f605-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f605-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5f605-107">DESCRIPTION</span></span>
<span data-ttu-id="5f605-108">Polecenie **cmdlet New-AzStorageQueueSASToken** generuje token podpisu dostępu udostępnionego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f605-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="5f605-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5f605-109">EXAMPLES</span></span>

### <span data-ttu-id="5f605-110">Przykład 1. Generowanie tokenu SAS kolejki z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="5f605-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="5f605-111">W tym przykładzie jest generowany token SAS kolejki z pełnymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="5f605-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="5f605-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f605-112">PARAMETERS</span></span>

### <span data-ttu-id="5f605-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="5f605-113">-Context</span></span>
<span data-ttu-id="5f605-114">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f605-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5f605-115">Możesz go utworzyć, New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f605-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5f605-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f605-116">-DefaultProfile</span></span>
<span data-ttu-id="5f605-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f605-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f605-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5f605-118">-ExpiryTime</span></span>
<span data-ttu-id="5f605-119">Określa, kiedy podpis dostępu udostępnionego jest już nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="5f605-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="5f605-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="5f605-120">-FullUri</span></span>
<span data-ttu-id="5f605-121">Wskazuje, że to polecenie cmdlet zwraca pełny adres URI obiektu blob i token podpisu dostępu udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="5f605-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="5f605-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5f605-122">-IPAddressOrRange</span></span>
<span data-ttu-id="5f605-123">Określa adres IP lub zakres adresów IP, z których mają być akceptowane żądania, na przykład 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="5f605-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="5f605-124">Zakres jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="5f605-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="5f605-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5f605-125">-Name</span></span>
<span data-ttu-id="5f605-126">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f605-126">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="5f605-127">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="5f605-127">-Permission</span></span>
<span data-ttu-id="5f605-128">Określa uprawnienia dla kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="5f605-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="5f605-129">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="5f605-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="5f605-130">— Zasady</span><span class="sxs-lookup"><span data-stu-id="5f605-130">-Policy</span></span>
<span data-ttu-id="5f605-131">Określa zasady dostępu przechowywanego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5f605-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="5f605-132">— Protokół</span><span class="sxs-lookup"><span data-stu-id="5f605-132">-Protocol</span></span>
<span data-ttu-id="5f605-133">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="5f605-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="5f605-134">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5f605-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="5f605-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="5f605-135">HttpsOnly</span></span>
* <span data-ttu-id="5f605-136">HttpsOrHttp Wartość domyślna to httpsorhttp.</span><span class="sxs-lookup"><span data-stu-id="5f605-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="5f605-137">— StartTime</span><span class="sxs-lookup"><span data-stu-id="5f605-137">-StartTime</span></span>
<span data-ttu-id="5f605-138">Określa, kiedy podpis dostępu udostępnionego stanie się prawidłowy.</span><span class="sxs-lookup"><span data-stu-id="5f605-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="5f605-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f605-139">CommonParameters</span></span>
<span data-ttu-id="5f605-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f605-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f605-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f605-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f605-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f605-142">INPUTS</span></span>

### <span data-ttu-id="5f605-143">System.String</span><span class="sxs-lookup"><span data-stu-id="5f605-143">System.String</span></span>

### <span data-ttu-id="5f605-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f605-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5f605-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f605-145">OUTPUTS</span></span>

### <span data-ttu-id="5f605-146">System.String</span><span class="sxs-lookup"><span data-stu-id="5f605-146">System.String</span></span>

## <span data-ttu-id="5f605-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5f605-147">NOTES</span></span>

## <span data-ttu-id="5f605-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f605-148">RELATED LINKS</span></span>
