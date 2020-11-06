---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
ms.openlocfilehash: 5bdd5e5d5212564afb1f9b06f220e8c452bcbbaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554272"
---
# <span data-ttu-id="a18bb-101">Get-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a18bb-101">Get-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="a18bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a18bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a18bb-103">Pobiera istniejący profil sieciowy zasób najwyższego poziomu</span><span class="sxs-lookup"><span data-stu-id="a18bb-103">Gets an existing network profile top level resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a18bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a18bb-104">SYNTAX</span></span>

### <span data-ttu-id="a18bb-105">NOEXPAND (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a18bb-105">NoExpand (Default)</span></span>
```
Get-AzureRmNetworkProfile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18bb-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="a18bb-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18bb-107">GetByResourceNameNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="a18bb-107">GetByResourceNameNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile [-ResourceGroupName <String>] [-Name <String>] -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18bb-108">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="a18bb-108">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18bb-109">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="a18bb-109">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a18bb-110">Opis</span><span class="sxs-lookup"><span data-stu-id="a18bb-110">DESCRIPTION</span></span>
<span data-ttu-id="a18bb-111">Polecenie cmdlet **Get-AzureRmNetworkProfile** pobiera istniejący profil sieci zasób najwyższego poziomu</span><span class="sxs-lookup"><span data-stu-id="a18bb-111">The **Get-AzureRmNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="a18bb-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a18bb-112">EXAMPLES</span></span>

### <span data-ttu-id="a18bb-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a18bb-113">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="a18bb-114">Spowoduje to pobranie profilu NP1 w grupie zasób RG1</span><span class="sxs-lookup"><span data-stu-id="a18bb-114">This retrieves the network profile np1 in resource group rg1</span></span>

## <span data-ttu-id="a18bb-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a18bb-115">PARAMETERS</span></span>

### <span data-ttu-id="a18bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18bb-116">-DefaultProfile</span></span>
<span data-ttu-id="a18bb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a18bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a18bb-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a18bb-118">-ExpandResource</span></span>
<span data-ttu-id="a18bb-119">Odwołanie do zasobu, które ma zostać rozwinięte.</span><span class="sxs-lookup"><span data-stu-id="a18bb-119">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceNameNoExpandParameterSet, GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a18bb-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a18bb-120">-Name</span></span>
<span data-ttu-id="a18bb-121">Nazwa profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a18bb-121">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a18bb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a18bb-122">-ResourceGroupName</span></span>
<span data-ttu-id="a18bb-123">Nazwa grupy zasobów profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a18bb-123">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a18bb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a18bb-124">-ResourceId</span></span>
<span data-ttu-id="a18bb-125">Identyfikator Menedżera zasobów platformy Azure profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a18bb-125">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a18bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18bb-126">CommonParameters</span></span>
<span data-ttu-id="a18bb-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a18bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18bb-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a18bb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18bb-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a18bb-129">INPUTS</span></span>

### <span data-ttu-id="a18bb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a18bb-130">System.String</span></span>

## <span data-ttu-id="a18bb-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a18bb-131">OUTPUTS</span></span>

### <span data-ttu-id="a18bb-132">Microsoft. Azure. Commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a18bb-132">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="a18bb-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a18bb-133">NOTES</span></span>

## <span data-ttu-id="a18bb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a18bb-134">RELATED LINKS</span></span>
