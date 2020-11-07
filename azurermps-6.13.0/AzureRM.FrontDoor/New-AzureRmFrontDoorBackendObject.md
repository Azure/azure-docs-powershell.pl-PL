---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
ms.openlocfilehash: 429db1fae2987531911bd4dfbd4c41daf66a5440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717403"
---
# <span data-ttu-id="c1b23-101">New-AzureRmFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="c1b23-101">New-AzureRmFrontDoorBackendObject</span></span>

## <span data-ttu-id="c1b23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1b23-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b23-103">Tworzenie obiektu PSBackend</span><span class="sxs-lookup"><span data-stu-id="c1b23-103">Create a PSBackend object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1b23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1b23-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-Priority <Int32>] [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1b23-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c1b23-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b23-106">Tworzenie obiektu PSBackend na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="c1b23-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="c1b23-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1b23-107">EXAMPLES</span></span>

### <span data-ttu-id="c1b23-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c1b23-108">Example 1</span></span>
```powershell
PS C:\>New-AzureRmFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="c1b23-109">Tworzenie obiektu PSBackend na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="c1b23-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="c1b23-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1b23-110">PARAMETERS</span></span>

### <span data-ttu-id="c1b23-111">-Address (adres)</span><span class="sxs-lookup"><span data-stu-id="c1b23-111">-Address</span></span>
<span data-ttu-id="c1b23-112">Lokalizacja wewnętrznej bazy danych (adres IP lub FQDN)</span><span class="sxs-lookup"><span data-stu-id="c1b23-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="c1b23-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="c1b23-113">-BackendHostHeader</span></span>
<span data-ttu-id="c1b23-114">Wartość, która ma być używana jako nagłówek hosta wysłany do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c1b23-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="c1b23-115">Wartość domyślna to adres zaplecza.</span><span class="sxs-lookup"><span data-stu-id="c1b23-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="c1b23-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b23-116">-DefaultProfile</span></span>
<span data-ttu-id="c1b23-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b23-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1b23-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c1b23-118">-EnabledState</span></span>
<span data-ttu-id="c1b23-119">Czy należy włączyć używanie tej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c1b23-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="c1b23-120">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="c1b23-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="c1b23-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="c1b23-121">-HttpPort</span></span>
<span data-ttu-id="c1b23-122">Numer portu TCP protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="c1b23-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="c1b23-123">Musi zawierać się między 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="c1b23-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="c1b23-124">Wartość domyślna to 80.</span><span class="sxs-lookup"><span data-stu-id="c1b23-124">Default value is 80.</span></span>

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

### <span data-ttu-id="c1b23-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="c1b23-125">-HttpsPort</span></span>
<span data-ttu-id="c1b23-126">Numer portu TCP protokołu TCP.</span><span class="sxs-lookup"><span data-stu-id="c1b23-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="c1b23-127">Musi zawierać się między 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="c1b23-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="c1b23-128">Wartość domyślna to 443</span><span class="sxs-lookup"><span data-stu-id="c1b23-128">Default value is 443</span></span>

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

### <span data-ttu-id="c1b23-129">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="c1b23-129">-Priority</span></span>
<span data-ttu-id="c1b23-130">Priorytet, który ma być używany do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c1b23-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="c1b23-131">Musi zawierać się między 1 a 5.</span><span class="sxs-lookup"><span data-stu-id="c1b23-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="c1b23-132">Wartość domyślna to 1</span><span class="sxs-lookup"><span data-stu-id="c1b23-132">Default value is 1</span></span>

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

### <span data-ttu-id="c1b23-133">-Waga</span><span class="sxs-lookup"><span data-stu-id="c1b23-133">-Weight</span></span>
<span data-ttu-id="c1b23-134">Waga tego punktu końcowego na potrzeby równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c1b23-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="c1b23-135">Musi zawierać się między 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="c1b23-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="c1b23-136">Wartość domyślna to 50</span><span class="sxs-lookup"><span data-stu-id="c1b23-136">Default value is 50</span></span>

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

### <span data-ttu-id="c1b23-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b23-137">CommonParameters</span></span>
<span data-ttu-id="c1b23-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b23-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b23-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1b23-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b23-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1b23-140">INPUTS</span></span>

### <span data-ttu-id="c1b23-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c1b23-141">None</span></span>

## <span data-ttu-id="c1b23-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1b23-142">OUTPUTS</span></span>

### <span data-ttu-id="c1b23-143">Microsoft. Azure. Commands. FrontDoor. models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="c1b23-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="c1b23-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1b23-144">NOTES</span></span>

## <span data-ttu-id="c1b23-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1b23-145">RELATED LINKS</span></span>

[<span data-ttu-id="c1b23-146">Nowe — AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="c1b23-146">New-AzureRmFrontDoorBackendPoolObject</span></span>](./New-AzureRmFrontDoorBackendPoolObject.md)
