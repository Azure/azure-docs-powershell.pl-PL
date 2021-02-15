---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193771"
---
# <span data-ttu-id="b26d9-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="b26d9-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="b26d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b26d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b26d9-103">Pobiera szczegółowe informacje bieżącego punktu połączenia z witryną z aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="b26d9-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="b26d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b26d9-104">SYNTAX</span></span>

### <span data-ttu-id="b26d9-105">ByP2SVpnGatewayName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b26d9-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b26d9-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="b26d9-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b26d9-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="b26d9-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b26d9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b26d9-108">DESCRIPTION</span></span>
<span data-ttu-id="b26d9-109">Polecenie **cmdlet Get-AzP2sVpnGatewayDetailedConnectionHealth** umożliwia uzyskiwanie szczegółowych informacji o bieżących połączeniach witryny z aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="b26d9-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="b26d9-110">Klient musi przekazać adres URL SAS, gdzie możemy umieścić te szczegółowe informacje o kondycji.</span><span class="sxs-lookup"><span data-stu-id="b26d9-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="b26d9-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b26d9-111">EXAMPLES</span></span>

### <span data-ttu-id="b26d9-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b26d9-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="b26d9-113">Polecenie **cmdlet Get-AzP2sVpnGatewayDetailedConnectionHealth** umożliwia uzyskiwanie szczegółowych informacji o bieżących połączeniach witryny z aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="b26d9-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="b26d9-114">Klient może pobrać szczegóły kondycji z przekazywanego adresu URL SAS.</span><span class="sxs-lookup"><span data-stu-id="b26d9-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="b26d9-115">Spowoduje to pokazanie informacji o każdym punkcie połączenia z witryną z nazwami użytkownika, bajtami w bajtach, przydzielonym adresem IP itp.</span><span class="sxs-lookup"><span data-stu-id="b26d9-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="b26d9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b26d9-116">PARAMETERS</span></span>

### <span data-ttu-id="b26d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26d9-117">-DefaultProfile</span></span>
<span data-ttu-id="b26d9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b26d9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b26d9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b26d9-119">-InputObject</span></span>
<span data-ttu-id="b26d9-120">Obiekt bramy sieci vpn p2s do modyfikacji</span><span class="sxs-lookup"><span data-stu-id="b26d9-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="b26d9-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b26d9-121">-Name</span></span>
<span data-ttu-id="b26d9-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b26d9-122">The resource name.</span></span>

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

### <span data-ttu-id="b26d9-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="b26d9-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="b26d9-124">Adres URL OutputBlob Sas, na który zostanie wpisana kondycja połączenia sieci vpn p2s.</span><span class="sxs-lookup"><span data-stu-id="b26d9-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="b26d9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b26d9-125">-ResourceGroupName</span></span>
<span data-ttu-id="b26d9-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b26d9-126">The resource group name.</span></span>

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

### <span data-ttu-id="b26d9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b26d9-127">-ResourceId</span></span>
<span data-ttu-id="b26d9-128">Identyfikator zasobu Azure p2SVpnGateway do modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="b26d9-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="b26d9-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="b26d9-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="b26d9-130">Lista nazw użytkowników sieci vpn P2S do filtrowania.</span><span class="sxs-lookup"><span data-stu-id="b26d9-130">The list of P2S vpn user names to filter.</span></span>

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

### <span data-ttu-id="b26d9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26d9-131">CommonParameters</span></span>
<span data-ttu-id="b26d9-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b26d9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26d9-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b26d9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26d9-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b26d9-134">INPUTS</span></span>

### <span data-ttu-id="b26d9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b26d9-135">System.String</span></span>
<span data-ttu-id="b26d9-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b26d9-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="b26d9-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b26d9-137">OUTPUTS</span></span>

### <span data-ttu-id="b26d9-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="b26d9-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="b26d9-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b26d9-139">NOTES</span></span>

## <span data-ttu-id="b26d9-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b26d9-140">RELATED LINKS</span></span>
