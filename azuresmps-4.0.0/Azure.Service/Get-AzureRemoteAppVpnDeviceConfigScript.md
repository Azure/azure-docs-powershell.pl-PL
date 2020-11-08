---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054591"
---
# <span data-ttu-id="755fc-101">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="755fc-101">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>

## <span data-ttu-id="755fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="755fc-102">SYNOPSIS</span></span>
<span data-ttu-id="755fc-103">Pobiera skrypt konfiguracji urządzenia sieci VPN funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="755fc-103">Retrieves the configuration script for an Azure RemoteApp VPN device.</span></span>

## <span data-ttu-id="755fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="755fc-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="755fc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="755fc-105">DESCRIPTION</span></span>
<span data-ttu-id="755fc-106">Polecenie cmdlet **Get-AzureRemoteAppVpnDeviceConfigScript** Pobiera skrypt konfiguracji urządzenia wirtualnej sieci prywatnej (VPN) usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="755fc-106">The **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet retrieves the configuration script for an Azure RemoteApp virtual private network (VPN) device.</span></span>

## <span data-ttu-id="755fc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="755fc-107">EXAMPLES</span></span>

### <span data-ttu-id="755fc-108">Przykład 1: uzyskiwanie skryptu konfiguracji dla urządzenia sieci VPN</span><span class="sxs-lookup"><span data-stu-id="755fc-108">Example 1: Get a configuration script for a VPN device</span></span>
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

<span data-ttu-id="755fc-109">To polecenie zwraca skrypt lub plik konfiguracji służący do skonfigurowania urządzenia sieci wirtualnej o nazwie ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="755fc-109">This command returns the script or configuration file used to configure the VPN device for the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="755fc-110">Ten skrypt lub plik konfiguracyjny powinien zostać uruchomiony lub załadowany na urządzenie sieci VPN w typowy sposób dla tego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="755fc-110">This script or configuration file should be run or loaded onto the VPN device in the typical manner for that device.</span></span>
<span data-ttu-id="755fc-111">Zapoznaj się z dostawcą urządzenia VPN, aby uzyskać unikatowe wymagania dla każdego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="755fc-111">Consult the VPN device vendor for the unique requirements for each device.</span></span>

## <span data-ttu-id="755fc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="755fc-112">PARAMETERS</span></span>

### <span data-ttu-id="755fc-113">-OSFamily</span><span class="sxs-lookup"><span data-stu-id="755fc-113">-OSFamily</span></span>
<span data-ttu-id="755fc-114">Określa rodzinę systemu operacyjnego (OS), która działa na platformie urządzenia.</span><span class="sxs-lookup"><span data-stu-id="755fc-114">Specifies the operating system (OS) family that runs on the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="755fc-115">-Platform</span><span class="sxs-lookup"><span data-stu-id="755fc-115">-Platform</span></span>
<span data-ttu-id="755fc-116">Określa platformę urządzenia.</span><span class="sxs-lookup"><span data-stu-id="755fc-116">Specifies the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="755fc-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="755fc-117">-Profile</span></span>
<span data-ttu-id="755fc-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="755fc-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="755fc-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="755fc-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="755fc-120">-Vendor</span><span class="sxs-lookup"><span data-stu-id="755fc-120">-Vendor</span></span>
<span data-ttu-id="755fc-121">Określa dostawcę urządzenia sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="755fc-121">Specifies the vendor of the VPN device.</span></span>

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

### <span data-ttu-id="755fc-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="755fc-122">-VNetName</span></span>
<span data-ttu-id="755fc-123">Określa nazwę sieci wirtualnej usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="755fc-123">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="755fc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755fc-124">CommonParameters</span></span>
<span data-ttu-id="755fc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755fc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755fc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="755fc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755fc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="755fc-127">INPUTS</span></span>

## <span data-ttu-id="755fc-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="755fc-128">OUTPUTS</span></span>

## <span data-ttu-id="755fc-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="755fc-129">NOTES</span></span>

## <span data-ttu-id="755fc-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="755fc-130">RELATED LINKS</span></span>

[<span data-ttu-id="755fc-131">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="755fc-131">Get-AzureRemoteAppVpnDevice</span></span>](./Get-AzureRemoteAppVpnDevice.md)


