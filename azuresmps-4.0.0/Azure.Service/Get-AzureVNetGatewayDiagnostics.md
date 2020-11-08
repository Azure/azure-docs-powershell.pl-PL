---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055243"
---
# <span data-ttu-id="cca80-101">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cca80-101">Get-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="cca80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cca80-102">SYNOPSIS</span></span>
<span data-ttu-id="cca80-103">Pobiera bieżący stan diagnostyki bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cca80-103">Gets the current state of diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="cca80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cca80-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cca80-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cca80-105">DESCRIPTION</span></span>
<span data-ttu-id="cca80-106">Polecenie cmdlet **Get-AzureVNetGatewayDiagnostics** Pobiera bieżący stan diagnostyki bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cca80-106">The **Get-AzureVNetGatewayDiagnostics** cmdlet gets the current state of diagnostics for a virtual network gateway.</span></span>
<span data-ttu-id="cca80-107">Jeśli obiekt BLOB (Binary Large Object) istnieje w miejscu, w którym na **początku AzureVNetGatewayDiagnostics** Zapisano poprzednią sesję diagnostyczną, to polecenie cmdlet zwróci również adres URL obiektu BLOB, w którym polecenie cmdlet jest zapisane w tej sesji diagnostycznej.</span><span class="sxs-lookup"><span data-stu-id="cca80-107">If a binary large object (blob) exists where the **Start-AzureVNetGatewayDiagnostics** saved a previous diagnostics session, this cmdlet also returns the URL of the blob where that cmdlet saved that diagnostics session.</span></span>

## <span data-ttu-id="cca80-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cca80-108">EXAMPLES</span></span>

## <span data-ttu-id="cca80-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cca80-109">PARAMETERS</span></span>

### <span data-ttu-id="cca80-110">-Profile</span><span class="sxs-lookup"><span data-stu-id="cca80-110">-Profile</span></span>
<span data-ttu-id="cca80-111">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cca80-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="cca80-112">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="cca80-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cca80-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="cca80-113">-VNetName</span></span>
<span data-ttu-id="cca80-114">Określa sieć wirtualną zawierającą wirtualną bramę sieciową, dla której to polecenie cmdlet pobiera diagnostykę.</span><span class="sxs-lookup"><span data-stu-id="cca80-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet gets diagnostics.</span></span>

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

### <span data-ttu-id="cca80-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca80-115">CommonParameters</span></span>
<span data-ttu-id="cca80-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cca80-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca80-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cca80-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca80-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cca80-118">INPUTS</span></span>

## <span data-ttu-id="cca80-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cca80-119">OUTPUTS</span></span>

## <span data-ttu-id="cca80-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cca80-120">NOTES</span></span>

## <span data-ttu-id="cca80-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cca80-121">RELATED LINKS</span></span>

[<span data-ttu-id="cca80-122">Start — AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cca80-122">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="cca80-123">Zatrzymaj — AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cca80-123">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


