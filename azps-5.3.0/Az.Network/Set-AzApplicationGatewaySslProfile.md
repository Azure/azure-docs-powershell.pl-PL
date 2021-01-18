---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 1763dfab6815efd625ff43ee248664a3f7b36cb9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503198"
---
# <span data-ttu-id="13ab1-101">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="13ab1-101">Set-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="13ab1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="13ab1-103">Aktualizuje profil protokołu SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="13ab1-103">Updates ssl profile for an application gateway.</span></span>

## <span data-ttu-id="13ab1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13ab1-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13ab1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13ab1-105">DESCRIPTION</span></span>
<span data-ttu-id="13ab1-106">Polecenie cmdlet **Set-AzApplicationGatewaySslProfile** aktualizuje profil SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="13ab1-106">The **Set-AzApplicationGatewaySslProfile** cmdlet updates the ssl profile for an Azure application gateway.</span></span>

## <span data-ttu-id="13ab1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13ab1-107">EXAMPLES</span></span>

### <span data-ttu-id="13ab1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13ab1-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "Profile01" -ClientAuthConfiguration $newclientconfig
```

<span data-ttu-id="13ab1-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="13ab1-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="13ab1-110">Drugie polecenie aktualizuje profil SSL bramy Application Gateway w zmiennej $AppGw, aby zaktualizować konfigurację uwierzytelniania klienta do nowej wartości przechowywanej w $newclientconfig.</span><span class="sxs-lookup"><span data-stu-id="13ab1-110">The second command updates the ssl profile of the application gateway in the $AppGw variable to update the client auth configuration to the new value stored in $newclientconfig.</span></span>

## <span data-ttu-id="13ab1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13ab1-111">PARAMETERS</span></span>

### <span data-ttu-id="13ab1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13ab1-112">-ApplicationGateway</span></span>
<span data-ttu-id="13ab1-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13ab1-113">The applicationGateway</span></span>

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

### <span data-ttu-id="13ab1-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="13ab1-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="13ab1-115">Ustawienia konfiguracji uwierzytelniania klienta</span><span class="sxs-lookup"><span data-stu-id="13ab1-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="13ab1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ab1-116">-DefaultProfile</span></span>
<span data-ttu-id="13ab1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13ab1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13ab1-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13ab1-118">-Name</span></span>
<span data-ttu-id="13ab1-119">Nazwa profilu SSL</span><span class="sxs-lookup"><span data-stu-id="13ab1-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="13ab1-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="13ab1-120">-SslPolicy</span></span>
<span data-ttu-id="13ab1-121">Zasady SSL</span><span class="sxs-lookup"><span data-stu-id="13ab1-121">SSL policy</span></span>

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

### <span data-ttu-id="13ab1-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="13ab1-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="13ab1-123">Łańcuch certyfikatu zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="13ab1-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="13ab1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ab1-124">CommonParameters</span></span>
<span data-ttu-id="13ab1-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13ab1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ab1-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13ab1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ab1-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13ab1-127">INPUTS</span></span>

### <span data-ttu-id="13ab1-128">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13ab1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13ab1-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13ab1-129">OUTPUTS</span></span>

### <span data-ttu-id="13ab1-130">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13ab1-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13ab1-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13ab1-131">NOTES</span></span>

## <span data-ttu-id="13ab1-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13ab1-132">RELATED LINKS</span></span>

[<span data-ttu-id="13ab1-133">Dodaj-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="13ab1-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="13ab1-134">Nowe — AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="13ab1-134">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="13ab1-135">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="13ab1-135">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="13ab1-136">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="13ab1-136">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)