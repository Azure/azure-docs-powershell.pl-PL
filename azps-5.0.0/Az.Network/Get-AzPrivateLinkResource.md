---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317179"
---
# <span data-ttu-id="a3a73-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a3a73-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="a3a73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3a73-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a73-103">Pobiera zasób link prywatny.</span><span class="sxs-lookup"><span data-stu-id="a3a73-103">Gets a private link resource.</span></span>

## <span data-ttu-id="a3a73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3a73-104">SYNTAX</span></span>

### <span data-ttu-id="a3a73-105">ByPrivateLinkResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a3a73-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3a73-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="a3a73-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="a3a73-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a3a73-107">DESCRIPTION</span></span>
<span data-ttu-id="a3a73-108">Polecenie cmdlet **Get-AzPrivateLinkResource** pobiera wszystkie zasoby linku do PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="a3a73-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="a3a73-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3a73-109">EXAMPLES</span></span>

### <span data-ttu-id="a3a73-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3a73-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="a3a73-111">W tym przykładzie podano listę wszystkich prywatnych zasobów linków nbelong do programu SQL Server o nazwie mySql.</span><span class="sxs-lookup"><span data-stu-id="a3a73-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="a3a73-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3a73-112">PARAMETERS</span></span>

### <span data-ttu-id="a3a73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a73-113">-DefaultProfile</span></span>
<span data-ttu-id="a3a73-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a73-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3a73-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a3a73-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="a3a73-116">Identyfikator Menedżera zasobów platformy Azure zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="a3a73-116">The Azure resource manager id of the private link resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a73-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="a3a73-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="a3a73-118">Typ zasobu link prywatny.</span><span class="sxs-lookup"><span data-stu-id="a3a73-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a73-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a73-119">-ResourceGroupName</span></span>
<span data-ttu-id="a3a73-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3a73-120">The resource group name.</span></span>

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

### <span data-ttu-id="a3a73-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a3a73-121">-ServiceName</span></span>
<span data-ttu-id="a3a73-122">Nazwa usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="a3a73-122">The private link service name.</span></span>

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

### <span data-ttu-id="a3a73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a73-123">CommonParameters</span></span>
<span data-ttu-id="a3a73-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3a73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a73-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3a73-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a73-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3a73-126">INPUTS</span></span>

### <span data-ttu-id="a3a73-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a3a73-127">System.String</span></span>

## <span data-ttu-id="a3a73-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3a73-128">OUTPUTS</span></span>

### <span data-ttu-id="a3a73-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3a73-129">System.Boolean</span></span>

## <span data-ttu-id="a3a73-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3a73-130">NOTES</span></span>

## <span data-ttu-id="a3a73-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3a73-131">RELATED LINKS</span></span>
