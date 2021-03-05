---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: d9a6936dec16f1723c0e74db7958093aca02ce97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983489"
---
# <span data-ttu-id="3e89e-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="3e89e-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="3e89e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e89e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e89e-103">Usuwa klucz aplikacji IotHub.</span><span class="sxs-lookup"><span data-stu-id="3e89e-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="3e89e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3e89e-104">SYNTAX</span></span>

### <span data-ttu-id="3e89e-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e89e-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e89e-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3e89e-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e89e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3e89e-107">DESCRIPTION</span></span>
<span data-ttu-id="3e89e-108">Usuwa klucz aplikacji IotHub.</span><span class="sxs-lookup"><span data-stu-id="3e89e-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="3e89e-109">Jeśli istnieje wiele klawiszy o tej samej nazwie, usunięty zostanie pierwszy z nich na liście.</span><span class="sxs-lookup"><span data-stu-id="3e89e-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="3e89e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3e89e-110">EXAMPLES</span></span>

### <span data-ttu-id="3e89e-111">Przykład 1. Usuwanie aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="3e89e-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="3e89e-112">Usuwa klucz o nazwie iothubowner1 z usługi IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="3e89e-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="3e89e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e89e-113">PARAMETERS</span></span>

### <span data-ttu-id="3e89e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e89e-114">-DefaultProfile</span></span>
<span data-ttu-id="3e89e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3e89e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e89e-116">— HubId</span><span class="sxs-lookup"><span data-stu-id="3e89e-116">-HubId</span></span>
<span data-ttu-id="3e89e-117">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="3e89e-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e89e-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3e89e-118">-KeyName</span></span>
<span data-ttu-id="3e89e-119">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="3e89e-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e89e-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3e89e-120">-Name</span></span>
<span data-ttu-id="3e89e-121">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="3e89e-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e89e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e89e-122">-ResourceGroupName</span></span>
<span data-ttu-id="3e89e-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3e89e-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e89e-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e89e-124">-Confirm</span></span>
<span data-ttu-id="3e89e-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3e89e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e89e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e89e-126">-WhatIf</span></span>
<span data-ttu-id="3e89e-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e89e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e89e-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3e89e-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e89e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e89e-129">CommonParameters</span></span>
<span data-ttu-id="3e89e-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e89e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e89e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e89e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e89e-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e89e-132">INPUTS</span></span>

### <span data-ttu-id="3e89e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3e89e-133">System.String</span></span>

## <span data-ttu-id="3e89e-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e89e-134">OUTPUTS</span></span>

### <span data-ttu-id="3e89e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3e89e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="3e89e-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3e89e-136">NOTES</span></span>

## <span data-ttu-id="3e89e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e89e-137">RELATED LINKS</span></span>
