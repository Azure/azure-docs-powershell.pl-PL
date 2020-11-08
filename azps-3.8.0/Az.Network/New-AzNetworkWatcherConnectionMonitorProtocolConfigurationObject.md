---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: 5a0994a5328390a928fd60cda8e8004deaaab162
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049984"
---
# <span data-ttu-id="5c144-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="5c144-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span></span>

## <span data-ttu-id="5c144-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c144-102">SYNOPSIS</span></span>
<span data-ttu-id="5c144-103">Tworzenie konfiguracji protokołu używanej do przeprowadzania oceny testowej przez protokoły TCP, HTTP lub ICMP.</span><span class="sxs-lookup"><span data-stu-id="5c144-103">Create protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="5c144-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c144-104">SYNTAX</span></span>

### <span data-ttu-id="5c144-105">PROTOKOŁ</span><span class="sxs-lookup"><span data-stu-id="5c144-105">TCP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <Int32>
 [-DisableTraceRoute] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c144-106">URL</span><span class="sxs-lookup"><span data-stu-id="5c144-106">HTTP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <Int32>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c144-107">Internetem</span><span class="sxs-lookup"><span data-stu-id="5c144-107">ICMP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c144-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5c144-108">DESCRIPTION</span></span>
<span data-ttu-id="5c144-109">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject umożliwia utworzenie konfiguracji protokołu służącej do przeprowadzania oceny testowej przez protokoły TCP, HTTP lub ICMP.</span><span class="sxs-lookup"><span data-stu-id="5c144-109">The New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdlet creates protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="5c144-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c144-110">EXAMPLES</span></span>

### <span data-ttu-id="5c144-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5c144-111">Example 1</span></span>
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

<span data-ttu-id="5c144-112">Port: 80 DisableTraceRoute: FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="5c144-112">Port              : 80 DisableTraceRoute : False</span></span>

## <span data-ttu-id="5c144-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c144-113">PARAMETERS</span></span>

### <span data-ttu-id="5c144-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c144-114">-DefaultProfile</span></span>
<span data-ttu-id="5c144-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c144-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c144-116">-DisableTraceRoute</span><span class="sxs-lookup"><span data-stu-id="5c144-116">-DisableTraceRoute</span></span>
<span data-ttu-id="5c144-117">Wartość wskazująca, czy ocena ścieżki z marszrutą śledzenia powinna być wyłączona.</span><span class="sxs-lookup"><span data-stu-id="5c144-117">Value indicating whether path evaluation with trace route should be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c144-118">-HttpProtocol</span><span class="sxs-lookup"><span data-stu-id="5c144-118">-HttpProtocol</span></span>
<span data-ttu-id="5c144-119">Przełącznik protokołu HTTP</span><span class="sxs-lookup"><span data-stu-id="5c144-119">HTTP protocol switch</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c144-120">-IcmpProtocol</span><span class="sxs-lookup"><span data-stu-id="5c144-120">-IcmpProtocol</span></span>
<span data-ttu-id="5c144-121">Przełącznik protokołu ICMP.</span><span class="sxs-lookup"><span data-stu-id="5c144-121">ICMP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c144-122">-Method</span><span class="sxs-lookup"><span data-stu-id="5c144-122">-Method</span></span>
<span data-ttu-id="5c144-123">Metoda HTTP, która ma zostać użyta.</span><span class="sxs-lookup"><span data-stu-id="5c144-123">The HTTP method to use.</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c144-124">-Path</span><span class="sxs-lookup"><span data-stu-id="5c144-124">-Path</span></span>
<span data-ttu-id="5c144-125">Składnik ścieżki identyfikatora URI.</span><span class="sxs-lookup"><span data-stu-id="5c144-125">The path component of the URI.</span></span> <span data-ttu-id="5c144-126">Na przykład \" /dir1/dir2 \" .</span><span class="sxs-lookup"><span data-stu-id="5c144-126">For instance, \"/dir1/dir2\".</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c144-127">-Port</span><span class="sxs-lookup"><span data-stu-id="5c144-127">-Port</span></span>
<span data-ttu-id="5c144-128">Port, z którym ma zostać nawiązane połączenie.</span><span class="sxs-lookup"><span data-stu-id="5c144-128">The port to connect to.</span></span>

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c144-129">-PreferHTTPS</span><span class="sxs-lookup"><span data-stu-id="5c144-129">-PreferHTTPS</span></span>
<span data-ttu-id="5c144-130">Wartość wskazująca, czy protokół HTTPS jest preferowany za pośrednictwem protokołu HTTP w przypadkach, gdy wybór jest niejawny.</span><span class="sxs-lookup"><span data-stu-id="5c144-130">Value indicating whether HTTPS is preferred over HTTP in cases where the choice is not explicit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c144-131">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="5c144-131">-RequestHeader</span></span>
<span data-ttu-id="5c144-132">Nagłówki HTTP do przesłania z żądaniem.</span><span class="sxs-lookup"><span data-stu-id="5c144-132">The HTTP headers to transmit with the request.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c144-133">-TcpProtocol</span><span class="sxs-lookup"><span data-stu-id="5c144-133">-TcpProtocol</span></span>
<span data-ttu-id="5c144-134">Przełącznik protokołu TCP.</span><span class="sxs-lookup"><span data-stu-id="5c144-134">TCP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c144-135">-ValidStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="5c144-135">-ValidStatusCodeRange</span></span>
<span data-ttu-id="5c144-136">Kody stanu HTTP, które powinny zostać rozpatrzone powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="5c144-136">HTTP status codes to consider successful.</span></span> <span data-ttu-id="5c144-137">Na przykład \" 2xx, 301-304418 \" .</span><span class="sxs-lookup"><span data-stu-id="5c144-137">For instance, \"2xx,301-304,418\".</span></span>

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c144-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c144-138">CommonParameters</span></span>
<span data-ttu-id="5c144-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c144-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c144-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c144-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c144-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c144-141">INPUTS</span></span>

### <span data-ttu-id="5c144-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5c144-142">None</span></span>

## <span data-ttu-id="5c144-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c144-143">OUTPUTS</span></span>

### <span data-ttu-id="5c144-144">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorTcpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c144-144">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorTcpConfiguration</span></span>

### <span data-ttu-id="5c144-145">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorHttpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c144-145">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorHttpConfiguration</span></span>

### <span data-ttu-id="5c144-146">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorIcmpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c144-146">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorIcmpConfiguration</span></span>

## <span data-ttu-id="5c144-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c144-147">NOTES</span></span>

## <span data-ttu-id="5c144-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c144-148">RELATED LINKS</span></span>
