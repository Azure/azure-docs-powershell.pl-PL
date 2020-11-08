---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054437"
---
# <span data-ttu-id="2f3d2-101">Reset-AzureRemoteAppVpnSharedKey</span><span class="sxs-lookup"><span data-stu-id="2f3d2-101">Reset-AzureRemoteAppVpnSharedKey</span></span>

## <span data-ttu-id="2f3d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="2f3d2-103">Resetuje klucz udostępniony sieci VPN funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2f3d2-103">Resets the Azure RemoteApp VPN shared key.</span></span>

## <span data-ttu-id="2f3d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f3d2-104">SYNTAX</span></span>

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f3d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f3d2-105">DESCRIPTION</span></span>
<span data-ttu-id="2f3d2-106">Polecenie cmdlet **Reset-AzureRemoteAppVpnSharedKey** resetuje klucz udostępniony wirtualnej sieci prywatnej (VPN) usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2f3d2-106">The **Reset-AzureRemoteAppVpnSharedKey** cmdlet resets the Azure RemoteApp virtual private network (VPN) shared key.</span></span>

## <span data-ttu-id="2f3d2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f3d2-107">EXAMPLES</span></span>

### <span data-ttu-id="2f3d2-108">Przykład 1: Resetowanie klucza udostępnionego w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2f3d2-108">Example 1: Reset the shared key on a virtual network</span></span>
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

<span data-ttu-id="2f3d2-109">To polecenie resetuje klucz udostępniony w sieci wirtualnej o nazwie ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="2f3d2-109">This command resets the shared key on the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="2f3d2-110">Połączenie VPN z siecią lokalną pozostaje w trybie offline, dopóki nie zostanie skonfigurowany nowy klucz udostępniony na urządzeniu sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="2f3d2-110">The VPN connection to the on-premises network remains offline until the new shared key is configured on the VPN device.</span></span>
<span data-ttu-id="2f3d2-111">Aby skonfigurować urządzenie sieci VPN, użyj polecenia cmdlet **Get-AzureRemoteAppVpnDeviceConfigScript** w celu pobrania odpowiedniego skryptu lub pliku konfiguracji dla urządzenia VPN, a następnie załaduj ten plik skryptu lub pliku konfiguracji na urządzenie sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="2f3d2-111">To configure the VPN device, use the **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet to retrieve the correct script or configuration file for your VPN device, then load that script or configuration file onto the VPN device.</span></span>

## <span data-ttu-id="2f3d2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f3d2-112">PARAMETERS</span></span>

### <span data-ttu-id="2f3d2-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="2f3d2-113">-Profile</span></span>
<span data-ttu-id="2f3d2-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f3d2-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f3d2-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2f3d2-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3d2-116">-VNetName</span><span class="sxs-lookup"><span data-stu-id="2f3d2-116">-VNetName</span></span>
<span data-ttu-id="2f3d2-117">Określa nazwę sieci wirtualnej usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2f3d2-117">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f3d2-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f3d2-118">-Confirm</span></span>
<span data-ttu-id="2f3d2-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f3d2-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3d2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f3d2-120">-WhatIf</span></span>
<span data-ttu-id="2f3d2-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f3d2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f3d2-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f3d2-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3d2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f3d2-123">CommonParameters</span></span>
<span data-ttu-id="2f3d2-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f3d2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f3d2-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f3d2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f3d2-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f3d2-126">INPUTS</span></span>

## <span data-ttu-id="2f3d2-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f3d2-127">OUTPUTS</span></span>

### <span data-ttu-id="2f3d2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2f3d2-128">System.String</span></span>

## <span data-ttu-id="2f3d2-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f3d2-129">NOTES</span></span>

## <span data-ttu-id="2f3d2-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f3d2-130">RELATED LINKS</span></span>

[<span data-ttu-id="2f3d2-131">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="2f3d2-131">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="2f3d2-132">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="2f3d2-132">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


