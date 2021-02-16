---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 1763dfab6815efd625ff43ee248664a3f7b36cb9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186891"
---
# <span data-ttu-id="8caaf-101">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8caaf-101">Set-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="8caaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8caaf-102">SYNOPSIS</span></span>
<span data-ttu-id="8caaf-103">Aktualizuje profil ssl dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8caaf-103">Updates ssl profile for an application gateway.</span></span>

## <span data-ttu-id="8caaf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8caaf-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8caaf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8caaf-105">DESCRIPTION</span></span>
<span data-ttu-id="8caaf-106">Polecenie **cmdlet Set-AzApplicationGatewaySslProfile** aktualizuje profil ssl bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8caaf-106">The **Set-AzApplicationGatewaySslProfile** cmdlet updates the ssl profile for an Azure application gateway.</span></span>

## <span data-ttu-id="8caaf-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8caaf-107">EXAMPLES</span></span>

### <span data-ttu-id="8caaf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8caaf-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "Profile01" -ClientAuthConfiguration $newclientconfig
```

<span data-ttu-id="8caaf-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="8caaf-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="8caaf-110">Drugie polecenie aktualizuje profil ssl bramy aplikacji w zmiennej $AppGw, aby zaktualizować konfigurację uwierzytelniania klienta do nowej wartości przechowywanej w $newclientconfig.</span><span class="sxs-lookup"><span data-stu-id="8caaf-110">The second command updates the ssl profile of the application gateway in the $AppGw variable to update the client auth configuration to the new value stored in $newclientconfig.</span></span>

## <span data-ttu-id="8caaf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8caaf-111">PARAMETERS</span></span>

### <span data-ttu-id="8caaf-112">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8caaf-112">-ApplicationGateway</span></span>
<span data-ttu-id="8caaf-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="8caaf-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8caaf-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8caaf-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="8caaf-115">Ustawienia konfiguracji uwierzytelniania klienta</span><span class="sxs-lookup"><span data-stu-id="8caaf-115">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8caaf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8caaf-116">-DefaultProfile</span></span>
<span data-ttu-id="8caaf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8caaf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8caaf-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8caaf-118">-Name</span></span>
<span data-ttu-id="8caaf-119">Nazwa profilu SSL</span><span class="sxs-lookup"><span data-stu-id="8caaf-119">The name of the SSL profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8caaf-120">- SslPolicy</span><span class="sxs-lookup"><span data-stu-id="8caaf-120">-SslPolicy</span></span>
<span data-ttu-id="8caaf-121">Zasady SSL</span><span class="sxs-lookup"><span data-stu-id="8caaf-121">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8caaf-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="8caaf-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="8caaf-123">Zaufane łańcuchy certyfikatów urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="8caaf-123">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8caaf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8caaf-124">CommonParameters</span></span>
<span data-ttu-id="8caaf-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8caaf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8caaf-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8caaf-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8caaf-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8caaf-127">INPUTS</span></span>

### <span data-ttu-id="8caaf-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8caaf-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8caaf-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8caaf-129">OUTPUTS</span></span>

### <span data-ttu-id="8caaf-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8caaf-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8caaf-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8caaf-131">NOTES</span></span>

## <span data-ttu-id="8caaf-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8caaf-132">RELATED LINKS</span></span>

[<span data-ttu-id="8caaf-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8caaf-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="8caaf-134">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8caaf-134">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="8caaf-135">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8caaf-135">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="8caaf-136">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8caaf-136">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)