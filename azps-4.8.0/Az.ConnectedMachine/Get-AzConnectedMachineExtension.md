---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222357"
---
# <span data-ttu-id="0eccb-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="0eccb-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="0eccb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0eccb-102">SYNOPSIS</span></span>
<span data-ttu-id="0eccb-103">Operacja pobierania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0eccb-103">The operation to get the extension.</span></span>

## <span data-ttu-id="0eccb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0eccb-104">SYNTAX</span></span>

### <span data-ttu-id="0eccb-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="0eccb-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0eccb-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="0eccb-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0eccb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0eccb-107">DESCRIPTION</span></span>
<span data-ttu-id="0eccb-108">Operacja pobierania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0eccb-108">The operation to get the extension.</span></span>

## <span data-ttu-id="0eccb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0eccb-109">EXAMPLES</span></span>

### <span data-ttu-id="0eccb-110">Przykład 1: wyświetlanie wszystkich rozszerzeń komputera</span><span class="sxs-lookup"><span data-stu-id="0eccb-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="0eccb-111">Lista wszystkich rozszerzeń określonego komputera.</span><span class="sxs-lookup"><span data-stu-id="0eccb-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="0eccb-112">Przykład 2: uzyskiwanie określonego rozszerzenia na komputerze</span><span class="sxs-lookup"><span data-stu-id="0eccb-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="0eccb-113">Pobiera określone rozszerzenie na komputerze.</span><span class="sxs-lookup"><span data-stu-id="0eccb-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="0eccb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0eccb-114">PARAMETERS</span></span>

### <span data-ttu-id="0eccb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eccb-115">-DefaultProfile</span></span>
<span data-ttu-id="0eccb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0eccb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccb-117">-Expand</span><span class="sxs-lookup"><span data-stu-id="0eccb-117">-Expand</span></span>
<span data-ttu-id="0eccb-118">Wyrażenie rozwijania, które ma zostać zastosowane w operacji.</span><span class="sxs-lookup"><span data-stu-id="0eccb-118">The expand expression to apply on the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccb-119">-NazwaKomputera</span><span class="sxs-lookup"><span data-stu-id="0eccb-119">-MachineName</span></span>
<span data-ttu-id="0eccb-120">Nazwa komputera zawierającego rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="0eccb-120">The name of the machine containing the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccb-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0eccb-121">-Name</span></span>
<span data-ttu-id="0eccb-122">Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="0eccb-122">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eccb-123">-ResourceGroupName</span></span>
<span data-ttu-id="0eccb-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0eccb-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccb-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0eccb-125">-SubscriptionId</span></span>
<span data-ttu-id="0eccb-126">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0eccb-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0eccb-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="0eccb-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eccb-128">CommonParameters</span></span>
<span data-ttu-id="0eccb-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eccb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eccb-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0eccb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eccb-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0eccb-131">INPUTS</span></span>

## <span data-ttu-id="0eccb-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0eccb-132">OUTPUTS</span></span>

### <span data-ttu-id="0eccb-133">Microsoft. Azure. PowerShell. polecenia. ConnectedMachine. models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="0eccb-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="0eccb-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0eccb-134">NOTES</span></span>

<span data-ttu-id="0eccb-135">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0eccb-135">ALIASES</span></span>

## <span data-ttu-id="0eccb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0eccb-136">RELATED LINKS</span></span>

