---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054985"
---
# <span data-ttu-id="6660d-101">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6660d-101">Stop-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="6660d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6660d-102">SYNOPSIS</span></span>
<span data-ttu-id="6660d-103">Zatrzymuje uruchomioną sesję diagnostyczną bramy VPN.</span><span class="sxs-lookup"><span data-stu-id="6660d-103">Stops a running VPN gateway diagnostics session.</span></span>

## <span data-ttu-id="6660d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6660d-104">SYNTAX</span></span>

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6660d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6660d-105">DESCRIPTION</span></span>
<span data-ttu-id="6660d-106">Polecenie cmdlet **stop-AzureVNetGatewayDiagnostics** zatrzymuje uruchomioną sesję diagnostyczną bramy wirtualnej sieci prywatnej (VPN).</span><span class="sxs-lookup"><span data-stu-id="6660d-106">The **Stop-AzureVNetGatewayDiagnostics** cmdlet stops a running virtual private network (VPN) gateway diagnostics session.</span></span>
<span data-ttu-id="6660d-107">To polecenie zapisuje wyniki sesji diagnostycznej na koncie magazynu, które jest określone przez polecenie cmdlet **Start-AzureVNetGatewayDiagnostics** .</span><span class="sxs-lookup"><span data-stu-id="6660d-107">This command saves the results of the diagnostics session to the storage account that the **Start-AzureVNetGatewayDiagnostics** cmdlet specifies.</span></span>

## <span data-ttu-id="6660d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6660d-108">EXAMPLES</span></span>

## <span data-ttu-id="6660d-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6660d-109">PARAMETERS</span></span>

### <span data-ttu-id="6660d-110">-Profile</span><span class="sxs-lookup"><span data-stu-id="6660d-110">-Profile</span></span>
<span data-ttu-id="6660d-111">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6660d-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6660d-112">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="6660d-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6660d-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="6660d-113">-VNetName</span></span>
<span data-ttu-id="6660d-114">Określa sieć wirtualną zawierającą wirtualną bramę sieciową, dla której to polecenie cmdlet przestanie diagnozowanie.</span><span class="sxs-lookup"><span data-stu-id="6660d-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet stops diagnostics.</span></span>

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

### <span data-ttu-id="6660d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6660d-115">CommonParameters</span></span>
<span data-ttu-id="6660d-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6660d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6660d-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6660d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6660d-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6660d-118">INPUTS</span></span>

## <span data-ttu-id="6660d-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6660d-119">OUTPUTS</span></span>

## <span data-ttu-id="6660d-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6660d-120">NOTES</span></span>

## <span data-ttu-id="6660d-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6660d-121">RELATED LINKS</span></span>

[<span data-ttu-id="6660d-122">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6660d-122">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="6660d-123">Start — AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6660d-123">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)


