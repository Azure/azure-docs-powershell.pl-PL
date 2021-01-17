---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350197"
---
# <span data-ttu-id="e1fd9-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e1fd9-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="e1fd9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="e1fd9-103">Umożliwia usunięcie prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="e1fd9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1fd9-104">SYNTAX</span></span>

### <span data-ttu-id="e1fd9-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e1fd9-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1fd9-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="e1fd9-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1fd9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e1fd9-107">DESCRIPTION</span></span>
<span data-ttu-id="e1fd9-108">Polecenie cmdlet **Remove-AzPrivateEndpointConnection** umożliwia usunięcie prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="e1fd9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1fd9-109">EXAMPLES</span></span>

### <span data-ttu-id="e1fd9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e1fd9-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="e1fd9-111">W tym przykładzie zostanie usunięte połączenie prywatne punktu końcowego o nazwie MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="e1fd9-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="e1fd9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1fd9-112">PARAMETERS</span></span>

### <span data-ttu-id="e1fd9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1fd9-113">-AsJob</span></span>
<span data-ttu-id="e1fd9-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e1fd9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1fd9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1fd9-115">-DefaultProfile</span></span>
<span data-ttu-id="e1fd9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1fd9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e1fd9-117">-Force</span></span>
<span data-ttu-id="e1fd9-118">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="e1fd9-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="e1fd9-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1fd9-119">-Name</span></span>
<span data-ttu-id="e1fd9-120">Nazwa połączenia prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-120">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="e1fd9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1fd9-121">-PassThru</span></span>
<span data-ttu-id="e1fd9-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1fd9-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1fd9-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="e1fd9-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="e1fd9-125">Typ zasobu link prywatny.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1fd9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1fd9-126">-ResourceGroupName</span></span>
<span data-ttu-id="e1fd9-127">Nazwa grupy zasobów połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="e1fd9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1fd9-128">-ResourceId</span></span>
<span data-ttu-id="e1fd9-129">Identyfikator Menedżera zasobów platformy Azure połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="e1fd9-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e1fd9-130">-ServiceName</span></span>
<span data-ttu-id="e1fd9-131">Nazwa usługi, do której należy połączenie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="e1fd9-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1fd9-132">-Confirm</span></span>
<span data-ttu-id="e1fd9-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fd9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1fd9-134">-WhatIf</span></span>
<span data-ttu-id="e1fd9-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1fd9-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fd9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1fd9-137">CommonParameters</span></span>
<span data-ttu-id="e1fd9-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1fd9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1fd9-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1fd9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1fd9-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1fd9-140">INPUTS</span></span>

### <span data-ttu-id="e1fd9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e1fd9-141">System.String</span></span>

## <span data-ttu-id="e1fd9-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1fd9-142">OUTPUTS</span></span>

### <span data-ttu-id="e1fd9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e1fd9-143">System.Boolean</span></span>

## <span data-ttu-id="e1fd9-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1fd9-144">NOTES</span></span>

## <span data-ttu-id="e1fd9-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1fd9-145">RELATED LINKS</span></span>

[<span data-ttu-id="e1fd9-146">Zatwierdzanie — AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e1fd9-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e1fd9-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e1fd9-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e1fd9-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e1fd9-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e1fd9-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e1fd9-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
