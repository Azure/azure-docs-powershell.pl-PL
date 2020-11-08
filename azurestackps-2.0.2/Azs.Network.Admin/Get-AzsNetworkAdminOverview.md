---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
schema: 2.0.0
ms.openlocfilehash: 8559b8cdde324c3927ac835f49291441a4e58847
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055934"
---
# <span data-ttu-id="963da-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="963da-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="963da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="963da-102">SYNOPSIS</span></span>
<span data-ttu-id="963da-103">Zapoznaj się z omówieniem stanu dostawcy zasobów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="963da-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="963da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="963da-104">SYNTAX</span></span>

### <span data-ttu-id="963da-105">Get (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="963da-105">Get (Default)</span></span>
```
Get-AzsNetworkAdminOverview [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="963da-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="963da-106">GetViaIdentity</span></span>
```
Get-AzsNetworkAdminOverview -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="963da-107">Opis</span><span class="sxs-lookup"><span data-stu-id="963da-107">DESCRIPTION</span></span>
<span data-ttu-id="963da-108">Zapoznaj się z omówieniem stanu dostawcy zasobów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="963da-108">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="963da-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="963da-109">EXAMPLES</span></span>

### <span data-ttu-id="963da-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="963da-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsNetworkAdminOverview
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
```



## <span data-ttu-id="963da-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="963da-111">PARAMETERS</span></span>

### <span data-ttu-id="963da-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="963da-112">-DefaultProfile</span></span>
<span data-ttu-id="963da-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="963da-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="963da-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="963da-114">-InputObject</span></span>
<span data-ttu-id="963da-115">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="963da-115">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="963da-116">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="963da-116">-SubscriptionId</span></span>
<span data-ttu-id="963da-117">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="963da-117">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="963da-118">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="963da-118">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="963da-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="963da-119">CommonParameters</span></span>
<span data-ttu-id="963da-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="963da-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="963da-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="963da-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="963da-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="963da-122">INPUTS</span></span>

### <span data-ttu-id="963da-123">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="963da-123">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="963da-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="963da-124">OUTPUTS</span></span>

### <span data-ttu-id="963da-125">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. IAdminOverview</span><span class="sxs-lookup"><span data-stu-id="963da-125">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IAdminOverview</span></span>



## <span data-ttu-id="963da-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="963da-126">NOTES</span></span>

<span data-ttu-id="963da-127">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="963da-127">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="963da-128">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="963da-128">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="963da-129">INPUTobject <INetworkAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="963da-129">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="963da-130">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="963da-130">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="963da-131">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="963da-131">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="963da-132">`[ResourceName <String>]`: Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="963da-132">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="963da-133">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="963da-133">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="963da-134">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="963da-134">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="963da-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="963da-135">RELATED LINKS</span></span>

