---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 82ff7d915a7ddc2d15655513dade28fc1e7ffff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223782"
---
# <span data-ttu-id="22ff4-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="22ff4-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="22ff4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="22ff4-103">Zdefiniuj nowe zasady podgrupa ruchu sieciowego pakietu Office 365, które mają być używane z witryną urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="22ff4-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="22ff4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22ff4-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22ff4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22ff4-105">DESCRIPTION</span></span>
<span data-ttu-id="22ff4-106">Polecenie New-AzOffice365PolicyProperties definiuje zasady podgrupa pakietu Office 365, które mają być używane woith witryny urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="22ff4-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used woith a Virtual Appliance site.</span></span> 

## <span data-ttu-id="22ff4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22ff4-107">EXAMPLES</span></span>

### <span data-ttu-id="22ff4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22ff4-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="22ff4-109">Tworzenie obiektu zasad podgrupa dla ruchu pakietu Office 365, który ma być wykorzystywany z poleceniami witryny urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="22ff4-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="22ff4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22ff4-110">PARAMETERS</span></span>

### <span data-ttu-id="22ff4-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="22ff4-111">-Allow</span></span>
<span data-ttu-id="22ff4-112">Podgrupa ruch kategorii Zezwól.</span><span class="sxs-lookup"><span data-stu-id="22ff4-112">Breakout the allow category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff4-113">-Wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="22ff4-113">-Default</span></span>
<span data-ttu-id="22ff4-114">Podgrupa domyślny ruch kategorii.</span><span class="sxs-lookup"><span data-stu-id="22ff4-114">Breakout the default category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ff4-115">-DefaultProfile</span></span>
<span data-ttu-id="22ff4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22ff4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff4-117">— Optymalizuj</span><span class="sxs-lookup"><span data-stu-id="22ff4-117">-Optimize</span></span>
<span data-ttu-id="22ff4-118">Podgrupa ruch kategorii.</span><span class="sxs-lookup"><span data-stu-id="22ff4-118">Breakout the optimize category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ff4-119">CommonParameters</span></span>
<span data-ttu-id="22ff4-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ff4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ff4-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22ff4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ff4-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22ff4-122">INPUTS</span></span>

### <span data-ttu-id="22ff4-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="22ff4-123">None</span></span>

## <span data-ttu-id="22ff4-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22ff4-124">OUTPUTS</span></span>

### <span data-ttu-id="22ff4-125">Microsoft. Azure. Commands. Network. models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="22ff4-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="22ff4-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22ff4-126">NOTES</span></span>

## <span data-ttu-id="22ff4-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22ff4-127">RELATED LINKS</span></span>
