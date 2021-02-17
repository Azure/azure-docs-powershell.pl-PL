---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188426"
---
# <span data-ttu-id="c33b1-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="c33b1-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="c33b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c33b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c33b1-103">Tworzenie obiektu PSBackend</span><span class="sxs-lookup"><span data-stu-id="c33b1-103">Create a PSBackend object</span></span>

## <span data-ttu-id="c33b1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c33b1-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c33b1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c33b1-105">DESCRIPTION</span></span>
<span data-ttu-id="c33b1-106">Tworzenie obiektu PSBackend do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="c33b1-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="c33b1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c33b1-107">EXAMPLES</span></span>

### <span data-ttu-id="c33b1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c33b1-108">Example 1</span></span>
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

<span data-ttu-id="c33b1-109">Tworzenie obiektu PSBackend do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="c33b1-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="c33b1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c33b1-110">PARAMETERS</span></span>

### <span data-ttu-id="c33b1-111">— Adres</span><span class="sxs-lookup"><span data-stu-id="c33b1-111">-Address</span></span>
<span data-ttu-id="c33b1-112">Lokalizacja zaplecza (adresu IP lub domeny FQDN)</span><span class="sxs-lookup"><span data-stu-id="c33b1-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="c33b1-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="c33b1-113">-BackendHostHeader</span></span>
<span data-ttu-id="c33b1-114">Wartość, która ma być używania jako nagłówek hosta wysyłany do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="c33b1-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="c33b1-115">Wartość domyślna to adres zaplecza.</span><span class="sxs-lookup"><span data-stu-id="c33b1-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="c33b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c33b1-116">-DefaultProfile</span></span>
<span data-ttu-id="c33b1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c33b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c33b1-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c33b1-118">-EnabledState</span></span>
<span data-ttu-id="c33b1-119">Czy można włączyć korzystanie z tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c33b1-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="c33b1-120">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="c33b1-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="c33b1-121">- HttpPort</span><span class="sxs-lookup"><span data-stu-id="c33b1-121">-HttpPort</span></span>
<span data-ttu-id="c33b1-122">Numer portu TCP protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="c33b1-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="c33b1-123">Musi to być od 1 do 65535.</span><span class="sxs-lookup"><span data-stu-id="c33b1-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="c33b1-124">Wartość domyślna to 80.</span><span class="sxs-lookup"><span data-stu-id="c33b1-124">Default value is 80.</span></span>

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

### <span data-ttu-id="c33b1-125">—HttpsPort</span><span class="sxs-lookup"><span data-stu-id="c33b1-125">-HttpsPort</span></span>
<span data-ttu-id="c33b1-126">Numer portu TCP protokołu HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c33b1-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="c33b1-127">Musi to być od 1 do 65535.</span><span class="sxs-lookup"><span data-stu-id="c33b1-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="c33b1-128">Wartość domyślna to 443</span><span class="sxs-lookup"><span data-stu-id="c33b1-128">Default value is 443</span></span>

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

### <span data-ttu-id="c33b1-129">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="c33b1-129">-Priority</span></span>
<span data-ttu-id="c33b1-130">Priorytet, który należy stosować do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c33b1-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="c33b1-131">Musi to być między 1 a 5.</span><span class="sxs-lookup"><span data-stu-id="c33b1-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="c33b1-132">Wartość domyślna to 1</span><span class="sxs-lookup"><span data-stu-id="c33b1-132">Default value is 1</span></span>

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

### <span data-ttu-id="c33b1-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="c33b1-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="c33b1-134">Alias zasobu Link prywatny.</span><span class="sxs-lookup"><span data-stu-id="c33b1-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="c33b1-135">Wypełnienie tego pola opcjonalnego oznacza, że ta zaplecza jest "prywatna"</span><span class="sxs-lookup"><span data-stu-id="c33b1-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="c33b1-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="c33b1-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="c33b1-137">Wiadomość niestandardowa dołączona do żądania zatwierdzenia połączenia z linkiem prywatnym</span><span class="sxs-lookup"><span data-stu-id="c33b1-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="c33b1-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="c33b1-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="c33b1-139">Lokalizacja zasobu Private Link.</span><span class="sxs-lookup"><span data-stu-id="c33b1-139">The Location of Private Link resource.</span></span> <span data-ttu-id="c33b1-140">Jeśli ustawiono wartość PrivateLinkResourceId, wymagana jest lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c33b1-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="c33b1-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="c33b1-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="c33b1-142">Identyfikator zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="c33b1-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="c33b1-143">Wypełnienie tego pola opcjonalnego oznacza, że ta zaplecza jest "prywatna"</span><span class="sxs-lookup"><span data-stu-id="c33b1-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="c33b1-144">— Waga</span><span class="sxs-lookup"><span data-stu-id="c33b1-144">-Weight</span></span>
<span data-ttu-id="c33b1-145">Waga tego punktu końcowego na potrzeby równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c33b1-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="c33b1-146">Musi to być od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="c33b1-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="c33b1-147">Wartość domyślna to 50</span><span class="sxs-lookup"><span data-stu-id="c33b1-147">Default value is 50</span></span>

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

### <span data-ttu-id="c33b1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33b1-148">CommonParameters</span></span>
<span data-ttu-id="c33b1-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c33b1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33b1-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c33b1-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33b1-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c33b1-151">INPUTS</span></span>

### <span data-ttu-id="c33b1-152">Brak</span><span class="sxs-lookup"><span data-stu-id="c33b1-152">None</span></span>

## <span data-ttu-id="c33b1-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c33b1-153">OUTPUTS</span></span>

### <span data-ttu-id="c33b1-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span><span class="sxs-lookup"><span data-stu-id="c33b1-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="c33b1-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c33b1-155">NOTES</span></span>

## <span data-ttu-id="c33b1-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c33b1-156">RELATED LINKS</span></span>

[<span data-ttu-id="c33b1-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="c33b1-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
