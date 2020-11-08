---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232598"
---
# <span data-ttu-id="58175-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="58175-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="58175-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58175-102">SYNOPSIS</span></span>
<span data-ttu-id="58175-103">Pobiera szczegółowe informacje o bieżącym punkcie połączenia z witrynami z P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="58175-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="58175-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58175-104">SYNTAX</span></span>

### <span data-ttu-id="58175-105">ByP2SVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="58175-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58175-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="58175-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58175-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="58175-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58175-108">Opis</span><span class="sxs-lookup"><span data-stu-id="58175-108">DESCRIPTION</span></span>
<span data-ttu-id="58175-109">Polecenie cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** umożliwia uzyskiwanie szczegółowych informacji o bieżących punktach połączeń z witrynami z P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="58175-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="58175-110">Klient musi przekazać adres URL SAS, w którym można umieścić te szczegółowe informacje o zdrowiu.</span><span class="sxs-lookup"><span data-stu-id="58175-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="58175-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58175-111">EXAMPLES</span></span>

### <span data-ttu-id="58175-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58175-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="58175-113">Polecenie cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** umożliwia uzyskiwanie szczegółowych informacji o bieżących punktach połączeń z witrynami z P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="58175-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="58175-114">Klient może pobrać szczegóły dotyczące kondycji z porzuconego pobranego adresu URL SAS.</span><span class="sxs-lookup"><span data-stu-id="58175-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="58175-115">Spowoduje to wyświetlenie informacji o poszczególnych punktach połączenia z nazwami użytkowników, liczbami bajtów, bajtów, przydzielonymi adresami IP itd.</span><span class="sxs-lookup"><span data-stu-id="58175-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="58175-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58175-116">PARAMETERS</span></span>

### <span data-ttu-id="58175-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58175-117">-DefaultProfile</span></span>
<span data-ttu-id="58175-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58175-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58175-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="58175-119">-InputObject</span></span>
<span data-ttu-id="58175-120">Obiekt bramy sieci VPN P2S, który ma zostać zmodyfikowany</span><span class="sxs-lookup"><span data-stu-id="58175-120">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58175-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58175-121">-Name</span></span>
<span data-ttu-id="58175-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="58175-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58175-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="58175-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="58175-124">Adres URL OutputBlob SAS, do którego zostaną zapisane kondycja połączenia VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="58175-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58175-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58175-125">-ResourceGroupName</span></span>
<span data-ttu-id="58175-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58175-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58175-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58175-127">-ResourceId</span></span>
<span data-ttu-id="58175-128">Identyfikator zasobu platformy Azure P2SVpnGateway, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="58175-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58175-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="58175-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="58175-130">Lista nazw użytkowników P2S sieci VPN do filtrowania.</span><span class="sxs-lookup"><span data-stu-id="58175-130">The list of P2S vpn user names to filter.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58175-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58175-131">CommonParameters</span></span>
<span data-ttu-id="58175-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58175-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58175-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58175-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58175-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58175-134">INPUTS</span></span>

### <span data-ttu-id="58175-135">System. String</span><span class="sxs-lookup"><span data-stu-id="58175-135">System.String</span></span>
<span data-ttu-id="58175-136">Microsoft. Azure. Commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="58175-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="58175-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58175-137">OUTPUTS</span></span>

### <span data-ttu-id="58175-138">Microsoft. Azure. Commands. Network. models. PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="58175-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="58175-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58175-139">NOTES</span></span>

## <span data-ttu-id="58175-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58175-140">RELATED LINKS</span></span>
