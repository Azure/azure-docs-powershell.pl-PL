---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: ea2d51b5e9fa7811832ae9ad47625ea1154fe3f9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891357"
---
# <span data-ttu-id="e4c3d-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e4c3d-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="e4c3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c3d-103">Usuwa klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="e4c3d-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="e4c3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4c3d-104">SYNTAX</span></span>

### <span data-ttu-id="e4c3d-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e4c3d-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4c3d-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e4c3d-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4c3d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e4c3d-107">DESCRIPTION</span></span>
<span data-ttu-id="e4c3d-108">Usuwa klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="e4c3d-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="e4c3d-109">Jeśli istnieje wiele kluczy o tej samej nazwie, zostanie usunięta pierwsza z nich na liście.</span><span class="sxs-lookup"><span data-stu-id="e4c3d-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="e4c3d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4c3d-110">EXAMPLES</span></span>

### <span data-ttu-id="e4c3d-111">Przykład 1 Usuwanie IotHub</span><span class="sxs-lookup"><span data-stu-id="e4c3d-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="e4c3d-112">Usuwa klucz o nazwie iothubowner1 z IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="e4c3d-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e4c3d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4c3d-113">PARAMETERS</span></span>

### <span data-ttu-id="e4c3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c3d-114">-DefaultProfile</span></span>
<span data-ttu-id="e4c3d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e4c3d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4c3d-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="e4c3d-116">-HubId</span></span>
<span data-ttu-id="e4c3d-117">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="e4c3d-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e4c3d-118">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="e4c3d-118">-KeyName</span></span>
<span data-ttu-id="e4c3d-119">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="e4c3d-119">Name of the Key</span></span>

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

### <span data-ttu-id="e4c3d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4c3d-120">-Name</span></span>
<span data-ttu-id="e4c3d-121">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="e4c3d-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="e4c3d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c3d-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4c3d-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e4c3d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e4c3d-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4c3d-124">-Confirm</span></span>
<span data-ttu-id="e4c3d-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4c3d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c3d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c3d-126">-WhatIf</span></span>
<span data-ttu-id="e4c3d-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4c3d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4c3d-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4c3d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c3d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c3d-129">CommonParameters</span></span>
<span data-ttu-id="e4c3d-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4c3d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c3d-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4c3d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c3d-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4c3d-132">INPUTS</span></span>

### <span data-ttu-id="e4c3d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e4c3d-133">System.String</span></span>

## <span data-ttu-id="e4c3d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4c3d-134">OUTPUTS</span></span>

### <span data-ttu-id="e4c3d-135">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e4c3d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e4c3d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4c3d-136">NOTES</span></span>

## <span data-ttu-id="e4c3d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4c3d-137">RELATED LINKS</span></span>
