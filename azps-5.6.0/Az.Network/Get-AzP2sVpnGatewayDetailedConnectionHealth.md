---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 17092ab89ded950678e60b079cd30558f7ce2aac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954250"
---
# <span data-ttu-id="c19bd-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="c19bd-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="c19bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c19bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c19bd-103">Pobiera szczegółowe informacje bieżącego punktu połączeń witryny z aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c19bd-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="c19bd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c19bd-104">SYNTAX</span></span>

### <span data-ttu-id="c19bd-105">ByP2SVpnGatewayName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c19bd-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c19bd-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c19bd-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c19bd-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c19bd-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c19bd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c19bd-108">DESCRIPTION</span></span>
<span data-ttu-id="c19bd-109">Polecenie **cmdlet Get-AzP2sVpnGatewayDetailedConnectionHealth** umożliwia uzyskiwanie szczegółowych informacji o bieżących połączeniach witryny z aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c19bd-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="c19bd-110">Klient musi przekazać adres URL SAS, gdzie możemy umieścić te szczegółowe informacje o kondycji.</span><span class="sxs-lookup"><span data-stu-id="c19bd-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="c19bd-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c19bd-111">EXAMPLES</span></span>

### <span data-ttu-id="c19bd-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c19bd-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="c19bd-113">Polecenie **cmdlet Get-AzP2sVpnGatewayDetailedConnectionHealth** umożliwia uzyskiwanie szczegółowych informacji o bieżących połączeniach witryny z aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c19bd-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="c19bd-114">Klient może pobrać szczegółowe informacje o kondycji z przekazywanego adresu URL SAS.</span><span class="sxs-lookup"><span data-stu-id="c19bd-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="c19bd-115">Spowoduje to pokazanie informacji o każdym punkcie połączenia z witryną z nazwami użytkownika, bajtami w bajtach, przydzielonym adresem IP itp.</span><span class="sxs-lookup"><span data-stu-id="c19bd-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="c19bd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c19bd-116">PARAMETERS</span></span>

### <span data-ttu-id="c19bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c19bd-117">-DefaultProfile</span></span>
<span data-ttu-id="c19bd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c19bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c19bd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c19bd-119">-InputObject</span></span>
<span data-ttu-id="c19bd-120">Obiekt bramy sieci vpn p2s do modyfikacji</span><span class="sxs-lookup"><span data-stu-id="c19bd-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="c19bd-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c19bd-121">-Name</span></span>
<span data-ttu-id="c19bd-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c19bd-122">The resource name.</span></span>

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

### <span data-ttu-id="c19bd-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="c19bd-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="c19bd-124">Adres URL OutputBlob Sas, na który zostanie wpisana kondycja połączenia sieci vpn p2s.</span><span class="sxs-lookup"><span data-stu-id="c19bd-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="c19bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c19bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="c19bd-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c19bd-126">The resource group name.</span></span>

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

### <span data-ttu-id="c19bd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c19bd-127">-ResourceId</span></span>
<span data-ttu-id="c19bd-128">Identyfikator zasobu Azure p2SVpnGateway do modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="c19bd-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="c19bd-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="c19bd-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="c19bd-130">Lista nazw użytkowników sieci vpn P2S do filtrowania.</span><span class="sxs-lookup"><span data-stu-id="c19bd-130">The list of P2S vpn user names to filter.</span></span>

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

### <span data-ttu-id="c19bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19bd-131">CommonParameters</span></span>
<span data-ttu-id="c19bd-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c19bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c19bd-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c19bd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19bd-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c19bd-134">INPUTS</span></span>

### <span data-ttu-id="c19bd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c19bd-135">System.String</span></span>
<span data-ttu-id="c19bd-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c19bd-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="c19bd-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c19bd-137">OUTPUTS</span></span>

### <span data-ttu-id="c19bd-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="c19bd-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="c19bd-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c19bd-139">NOTES</span></span>

## <span data-ttu-id="c19bd-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c19bd-140">RELATED LINKS</span></span>
