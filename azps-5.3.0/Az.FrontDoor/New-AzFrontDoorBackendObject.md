---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501053"
---
# <span data-ttu-id="f70be-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="f70be-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="f70be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f70be-102">SYNOPSIS</span></span>
<span data-ttu-id="f70be-103">Tworzenie obiektu PSBackend</span><span class="sxs-lookup"><span data-stu-id="f70be-103">Create a PSBackend object</span></span>

## <span data-ttu-id="f70be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f70be-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f70be-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f70be-105">DESCRIPTION</span></span>
<span data-ttu-id="f70be-106">Tworzenie obiektu PSBackend na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="f70be-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="f70be-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f70be-107">EXAMPLES</span></span>

### <span data-ttu-id="f70be-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f70be-108">Example 1</span></span>
```powershell
PS C:\>New-AzFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="f70be-109">Tworzenie obiektu PSBackend na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="f70be-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="f70be-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f70be-110">PARAMETERS</span></span>

### <span data-ttu-id="f70be-111">-Address (adres)</span><span class="sxs-lookup"><span data-stu-id="f70be-111">-Address</span></span>
<span data-ttu-id="f70be-112">Lokalizacja wewnętrznej bazy danych (adres IP lub FQDN)</span><span class="sxs-lookup"><span data-stu-id="f70be-112">Location of the backend (IP address or FQDN)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f70be-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="f70be-113">-BackendHostHeader</span></span>
<span data-ttu-id="f70be-114">Wartość, która ma być używana jako nagłówek hosta wysłany do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f70be-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="f70be-115">Wartość domyślna to adres zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f70be-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="f70be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f70be-116">-DefaultProfile</span></span>
<span data-ttu-id="f70be-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f70be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f70be-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="f70be-118">-EnabledState</span></span>
<span data-ttu-id="f70be-119">Czy należy włączyć używanie tej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f70be-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="f70be-120">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="f70be-120">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f70be-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="f70be-121">-HttpPort</span></span>
<span data-ttu-id="f70be-122">Numer portu TCP protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="f70be-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="f70be-123">Musi zawierać się między 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="f70be-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="f70be-124">Wartość domyślna to 80.</span><span class="sxs-lookup"><span data-stu-id="f70be-124">Default value is 80.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f70be-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="f70be-125">-HttpsPort</span></span>
<span data-ttu-id="f70be-126">Numer portu TCP protokołu TCP.</span><span class="sxs-lookup"><span data-stu-id="f70be-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="f70be-127">Musi zawierać się między 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="f70be-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="f70be-128">Wartość domyślna to 443</span><span class="sxs-lookup"><span data-stu-id="f70be-128">Default value is 443</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f70be-129">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="f70be-129">-Priority</span></span>
<span data-ttu-id="f70be-130">Priorytet, który ma być używany do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f70be-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="f70be-131">Musi zawierać się między 1 a 5.</span><span class="sxs-lookup"><span data-stu-id="f70be-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="f70be-132">Wartość domyślna to 1</span><span class="sxs-lookup"><span data-stu-id="f70be-132">Default value is 1</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f70be-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="f70be-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="f70be-134">Alias zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="f70be-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="f70be-135">Wypełnianie tego pola opcjonalnego oznacza, że ta wewnętrzna baza danych jest "prywatna"</span><span class="sxs-lookup"><span data-stu-id="f70be-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="f70be-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="f70be-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="f70be-137">Niestandardowa wiadomość, która ma być uwzględniona w żądaniu zatwierdzenia w celu nawiązania połączenia z prywatnym linkiem</span><span class="sxs-lookup"><span data-stu-id="f70be-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="f70be-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="f70be-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="f70be-139">Lokalizacja zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="f70be-139">The Location of Private Link resource.</span></span> <span data-ttu-id="f70be-140">Lokalizacja jest wymagana w przypadku ustawienia PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f70be-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="f70be-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f70be-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="f70be-142">Identyfikator zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="f70be-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="f70be-143">Wypełnianie tego pola opcjonalnego oznacza, że ta wewnętrzna baza danych jest "prywatna"</span><span class="sxs-lookup"><span data-stu-id="f70be-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="f70be-144">-Waga</span><span class="sxs-lookup"><span data-stu-id="f70be-144">-Weight</span></span>
<span data-ttu-id="f70be-145">Waga tego punktu końcowego na potrzeby równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f70be-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="f70be-146">Musi zawierać się między 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="f70be-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="f70be-147">Wartość domyślna to 50</span><span class="sxs-lookup"><span data-stu-id="f70be-147">Default value is 50</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f70be-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f70be-148">CommonParameters</span></span>
<span data-ttu-id="f70be-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f70be-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f70be-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f70be-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f70be-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f70be-151">INPUTS</span></span>

### <span data-ttu-id="f70be-152">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f70be-152">None</span></span>

## <span data-ttu-id="f70be-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f70be-153">OUTPUTS</span></span>

### <span data-ttu-id="f70be-154">Microsoft. Azure. Commands. FrontDoor. models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="f70be-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="f70be-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f70be-155">NOTES</span></span>

## <span data-ttu-id="f70be-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f70be-156">RELATED LINKS</span></span>

[<span data-ttu-id="f70be-157">Nowe — AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="f70be-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
