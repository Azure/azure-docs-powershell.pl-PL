---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: d5b7a2d0713fec7c11f33d778cf9708c253f153a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965914"
---
# <span data-ttu-id="bc834-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="bc834-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="bc834-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc834-102">SYNOPSIS</span></span>
<span data-ttu-id="bc834-103">Tworzenie obiektu PSBackend</span><span class="sxs-lookup"><span data-stu-id="bc834-103">Create a PSBackend object</span></span>

## <span data-ttu-id="bc834-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc834-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc834-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc834-105">DESCRIPTION</span></span>
<span data-ttu-id="bc834-106">Tworzenie obiektu PSBackend do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="bc834-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="bc834-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc834-107">EXAMPLES</span></span>

### <span data-ttu-id="bc834-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bc834-108">Example 1</span></span>
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

<span data-ttu-id="bc834-109">Tworzenie obiektu PSBackend do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="bc834-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="bc834-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc834-110">PARAMETERS</span></span>

### <span data-ttu-id="bc834-111">— Adres</span><span class="sxs-lookup"><span data-stu-id="bc834-111">-Address</span></span>
<span data-ttu-id="bc834-112">Lokalizacja zaplecza (adresu IP lub domeny FQDN)</span><span class="sxs-lookup"><span data-stu-id="bc834-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="bc834-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="bc834-113">-BackendHostHeader</span></span>
<span data-ttu-id="bc834-114">Wartość, która ma być używania jako nagłówek hosta wysyłany do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="bc834-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="bc834-115">Wartość domyślna to adres zaplecza.</span><span class="sxs-lookup"><span data-stu-id="bc834-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="bc834-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc834-116">-DefaultProfile</span></span>
<span data-ttu-id="bc834-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc834-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc834-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="bc834-118">-EnabledState</span></span>
<span data-ttu-id="bc834-119">Czy można włączyć korzystanie z tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bc834-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="bc834-120">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="bc834-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="bc834-121">- HttpPort</span><span class="sxs-lookup"><span data-stu-id="bc834-121">-HttpPort</span></span>
<span data-ttu-id="bc834-122">Numer portu TCP protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="bc834-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="bc834-123">Musi to być między 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="bc834-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="bc834-124">Wartość domyślna to 80.</span><span class="sxs-lookup"><span data-stu-id="bc834-124">Default value is 80.</span></span>

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

### <span data-ttu-id="bc834-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="bc834-125">-HttpsPort</span></span>
<span data-ttu-id="bc834-126">Numer portu TCP protokołu HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bc834-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="bc834-127">Musi to być między 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="bc834-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="bc834-128">Wartość domyślna to 443</span><span class="sxs-lookup"><span data-stu-id="bc834-128">Default value is 443</span></span>

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

### <span data-ttu-id="bc834-129">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="bc834-129">-Priority</span></span>
<span data-ttu-id="bc834-130">Priorytet używania do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="bc834-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="bc834-131">Musi to być od 1 do 5.</span><span class="sxs-lookup"><span data-stu-id="bc834-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="bc834-132">Wartość domyślna to 1</span><span class="sxs-lookup"><span data-stu-id="bc834-132">Default value is 1</span></span>

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

### <span data-ttu-id="bc834-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="bc834-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="bc834-134">Alias zasobu Link prywatny.</span><span class="sxs-lookup"><span data-stu-id="bc834-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="bc834-135">Wypełnienie tego pola opcjonalnego oznacza, że ta zaplecza jest "prywatna"</span><span class="sxs-lookup"><span data-stu-id="bc834-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="bc834-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="bc834-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="bc834-137">Wiadomość niestandardowa dołączona do żądania zatwierdzenia połączenia z linkiem prywatnym</span><span class="sxs-lookup"><span data-stu-id="bc834-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="bc834-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="bc834-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="bc834-139">Lokalizacja zasobu Private Link.</span><span class="sxs-lookup"><span data-stu-id="bc834-139">The Location of Private Link resource.</span></span> <span data-ttu-id="bc834-140">Jeśli ustawiono wartość PrivateLinkResourceId, wymagana jest lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bc834-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="bc834-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="bc834-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="bc834-142">Identyfikator zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="bc834-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="bc834-143">Wypełnienie tego pola opcjonalnego oznacza, że ta zaplecza jest "prywatna"</span><span class="sxs-lookup"><span data-stu-id="bc834-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="bc834-144">— Waga</span><span class="sxs-lookup"><span data-stu-id="bc834-144">-Weight</span></span>
<span data-ttu-id="bc834-145">Waga tego punktu końcowego na potrzeby równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="bc834-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="bc834-146">Musi to być od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="bc834-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="bc834-147">Wartość domyślna to 50</span><span class="sxs-lookup"><span data-stu-id="bc834-147">Default value is 50</span></span>

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

### <span data-ttu-id="bc834-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc834-148">CommonParameters</span></span>
<span data-ttu-id="bc834-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc834-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc834-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc834-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc834-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc834-151">INPUTS</span></span>

### <span data-ttu-id="bc834-152">Brak</span><span class="sxs-lookup"><span data-stu-id="bc834-152">None</span></span>

## <span data-ttu-id="bc834-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc834-153">OUTPUTS</span></span>

### <span data-ttu-id="bc834-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span><span class="sxs-lookup"><span data-stu-id="bc834-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="bc834-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc834-155">NOTES</span></span>

## <span data-ttu-id="bc834-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc834-156">RELATED LINKS</span></span>

[<span data-ttu-id="bc834-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="bc834-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
