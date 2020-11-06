---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
ms.openlocfilehash: 08e68a878267f706c280c8d461e8c904141cd06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546440"
---
# <span data-ttu-id="aa14d-101">Get-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="aa14d-101">Get-AzureRmSignalR</span></span>

## <span data-ttu-id="aa14d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa14d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa14d-103">Uzyskaj określoną usługę sygnalizującą lub wszystkie usługi sygnalizujące w grupie zasobów lub abonament.</span><span class="sxs-lookup"><span data-stu-id="aa14d-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa14d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa14d-104">SYNTAX</span></span>

### <span data-ttu-id="aa14d-105">ListSignalRServiceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aa14d-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa14d-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa14d-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa14d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa14d-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa14d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aa14d-108">DESCRIPTION</span></span>
<span data-ttu-id="aa14d-109">Uzyskaj określoną usługę sygnalizującą lub wszystkie usługi sygnalizujące w grupie zasobów lub abonament.</span><span class="sxs-lookup"><span data-stu-id="aa14d-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="aa14d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa14d-110">EXAMPLES</span></span>

### <span data-ttu-id="aa14d-111">Uzyskiwanie wszystkich usług sygnalizacji w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="aa14d-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzureRmSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="aa14d-112">Uzyskiwanie wszystkich usług sygnalizacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="aa14d-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="aa14d-113">Uzyskaj określoną usługę sygnalizującą</span><span class="sxs-lookup"><span data-stu-id="aa14d-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="aa14d-114">Uzyskiwanie określonej usługi sygnalizującego z domyślnej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="aa14d-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="aa14d-115">Domyślna grupa zasobów może być ustawiona przez `Set-AzureRmDefault -ResourceGroupName myResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="aa14d-115">The default resource group can be set by `Set-AzureRmDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="aa14d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa14d-116">PARAMETERS</span></span>

### <span data-ttu-id="aa14d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa14d-117">-DefaultProfile</span></span>
<span data-ttu-id="aa14d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa14d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa14d-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa14d-119">-Name</span></span>
<span data-ttu-id="aa14d-120">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="aa14d-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa14d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa14d-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa14d-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa14d-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa14d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa14d-123">-ResourceId</span></span>
<span data-ttu-id="aa14d-124">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="aa14d-124">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa14d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa14d-125">CommonParameters</span></span>
<span data-ttu-id="aa14d-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa14d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa14d-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa14d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa14d-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa14d-128">INPUTS</span></span>

### <span data-ttu-id="aa14d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aa14d-129">System.String</span></span>
<span data-ttu-id="aa14d-130">Parametry: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aa14d-130">Parameters: ResourceId (ByValue)</span></span>

## <span data-ttu-id="aa14d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa14d-131">OUTPUTS</span></span>

### <span data-ttu-id="aa14d-132">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="aa14d-132">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="aa14d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa14d-133">NOTES</span></span>

## <span data-ttu-id="aa14d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa14d-134">RELATED LINKS</span></span>
