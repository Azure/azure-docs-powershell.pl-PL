---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4E19A767-8233-42A0-95C5-1547B4DF297E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c08105f8083b6b2e132c3b8e61c92627572305
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055300"
---
# <span data-ttu-id="c3fbd-101">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c3fbd-101">Get-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="c3fbd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fbd-103">Pobiera szczegóły grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="c3fbd-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="c3fbd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3fbd-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroup [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c3fbd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="c3fbd-106">Polecenie cmdlet **Get-AzureNetworkSecurityGroup** zwraca szczegóły grupy zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="c3fbd-106">The **Get-AzureNetworkSecurityGroup** cmdlet returns details for an Azure network security group.</span></span>
<span data-ttu-id="c3fbd-107">Określ *szczegółowy* parametr, aby wyświetlić reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="c3fbd-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="c3fbd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3fbd-108">EXAMPLES</span></span>

## <span data-ttu-id="c3fbd-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3fbd-109">PARAMETERS</span></span>

### <span data-ttu-id="c3fbd-110">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c3fbd-110">-Detailed</span></span>
<span data-ttu-id="c3fbd-111">Wskazuje, że to polecenie cmdlet zwraca reguły zabezpieczeń sieci dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="c3fbd-111">Indicates that this cmdlet returns the network security rules for the network security group.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fbd-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c3fbd-112">-Name</span></span>
<span data-ttu-id="c3fbd-113">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet pobiera.</span><span class="sxs-lookup"><span data-stu-id="c3fbd-113">Specifies the name of the network security group that this cmdlet gets.</span></span>

> [!NOTE]
> <span data-ttu-id="c3fbd-114">Po utworzeniu klasycznej grupy zabezpieczeń sieci w grupie zasobów innej niż ***Domyślna — sieci*** korzystających z usługi Azure Portal należy użyć następującej składni programu PowerShell: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'` .</span><span class="sxs-lookup"><span data-stu-id="c3fbd-114">When a classic network security group is created in a resource group other than ***Default-Networking*** using the Azure portal, you must use the following PowerShell syntax: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fbd-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="c3fbd-115">-Profile</span></span>
<span data-ttu-id="c3fbd-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3fbd-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3fbd-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c3fbd-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c3fbd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fbd-118">CommonParameters</span></span>
<span data-ttu-id="c3fbd-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3fbd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3fbd-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3fbd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fbd-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3fbd-121">INPUTS</span></span>

## <span data-ttu-id="c3fbd-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3fbd-122">OUTPUTS</span></span>

## <span data-ttu-id="c3fbd-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3fbd-123">NOTES</span></span>

## <span data-ttu-id="c3fbd-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3fbd-124">RELATED LINKS</span></span>

[<span data-ttu-id="c3fbd-125">Nowe — AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c3fbd-125">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="c3fbd-126">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c3fbd-126">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)

