---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7504da022a5cf1310a375bed40370d71d60f205a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870111"
---
# <span data-ttu-id="41c19-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="41c19-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="41c19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41c19-102">SYNOPSIS</span></span>
<span data-ttu-id="41c19-103">Pobiera prywatny zasób połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="41c19-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="41c19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41c19-104">SYNTAX</span></span>

### <span data-ttu-id="41c19-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="41c19-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41c19-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="41c19-106">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41c19-107">Opis</span><span class="sxs-lookup"><span data-stu-id="41c19-107">DESCRIPTION</span></span>
<span data-ttu-id="41c19-108">Polecenie cmdlet **Get-AzPrivateEndpointConnection** pobiera prywatny zasób połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="41c19-108">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="41c19-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41c19-109">EXAMPLES</span></span>

### <span data-ttu-id="41c19-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="41c19-110">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="41c19-111">W tym przykładzie jest uzyskiwane połączenie prywatne punktu końcowego o nazwie MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="41c19-111">This example get a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="41c19-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41c19-112">PARAMETERS</span></span>

### <span data-ttu-id="41c19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c19-113">-DefaultProfile</span></span>
<span data-ttu-id="41c19-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41c19-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41c19-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="41c19-115">-Description</span></span>
<span data-ttu-id="41c19-116">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="41c19-116">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c19-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41c19-117">-Name</span></span>
<span data-ttu-id="41c19-118">Nazwa połączenia prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="41c19-118">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c19-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41c19-119">-ResourceGroupName</span></span>
<span data-ttu-id="41c19-120">Nazwa grupy zasobów połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="41c19-120">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c19-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41c19-121">-ResourceId</span></span>
<span data-ttu-id="41c19-122">Identyfikator Menedżera zasobów platformy Azure połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="41c19-122">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c19-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="41c19-123">-ServiceName</span></span>
<span data-ttu-id="41c19-124">Nazwa usługi linku prywatnego z połączeniem prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="41c19-124">The name of the private link service that has the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c19-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c19-125">CommonParameters</span></span>
<span data-ttu-id="41c19-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41c19-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c19-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41c19-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c19-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41c19-128">INPUTS</span></span>

### <span data-ttu-id="41c19-129">System. String</span><span class="sxs-lookup"><span data-stu-id="41c19-129">System.String</span></span>

## <span data-ttu-id="41c19-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41c19-130">OUTPUTS</span></span>

### <span data-ttu-id="41c19-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41c19-131">System.Boolean</span></span>

## <span data-ttu-id="41c19-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41c19-132">NOTES</span></span>

## <span data-ttu-id="41c19-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41c19-133">RELATED LINKS</span></span>

[<span data-ttu-id="41c19-134">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="41c19-134">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
