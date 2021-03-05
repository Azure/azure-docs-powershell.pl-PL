---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: b6a2e27f18a0ae9b7c98239d5acd1073922e149e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006666"
---
# <span data-ttu-id="f2a52-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="f2a52-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="f2a52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2a52-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a52-103">Tworzy konto usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="f2a52-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="f2a52-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2a52-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2a52-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2a52-105">DESCRIPTION</span></span>
<span data-ttu-id="f2a52-106">Polecenie New-AzMapsAccount cmdlet tworzy konto usługi Azure Maps z określoną określonej wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="f2a52-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="f2a52-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2a52-107">EXAMPLES</span></span>

### <span data-ttu-id="f2a52-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2a52-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="f2a52-109">Tworzy nowe konto usługi Azure Maps o nazwie MyAccount w grupie zasobów MyResourceGroup z sku S0 i tagiem.</span><span class="sxs-lookup"><span data-stu-id="f2a52-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="f2a52-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2a52-110">PARAMETERS</span></span>

### <span data-ttu-id="f2a52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a52-111">-DefaultProfile</span></span>
<span data-ttu-id="f2a52-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2a52-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2a52-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f2a52-113">-Force</span></span>
<span data-ttu-id="f2a52-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f2a52-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f2a52-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f2a52-115">-Name</span></span>
<span data-ttu-id="f2a52-116">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="f2a52-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2a52-117">-ResourceGroupName</span></span>
<span data-ttu-id="f2a52-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2a52-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a52-119">-SKUName</span><span class="sxs-lookup"><span data-stu-id="f2a52-119">-SkuName</span></span>
<span data-ttu-id="f2a52-120">Nazwa SKU konta mapy.</span><span class="sxs-lookup"><span data-stu-id="f2a52-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a52-121">— Tag</span><span class="sxs-lookup"><span data-stu-id="f2a52-121">-Tag</span></span>
<span data-ttu-id="f2a52-122">Tagi konta mapy.</span><span class="sxs-lookup"><span data-stu-id="f2a52-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a52-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2a52-123">-Confirm</span></span>
<span data-ttu-id="f2a52-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f2a52-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2a52-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2a52-125">-WhatIf</span></span>
<span data-ttu-id="f2a52-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2a52-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2a52-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f2a52-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2a52-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a52-128">CommonParameters</span></span>
<span data-ttu-id="f2a52-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2a52-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a52-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2a52-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a52-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2a52-131">INPUTS</span></span>

### <span data-ttu-id="f2a52-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f2a52-132">System.String</span></span>

## <span data-ttu-id="f2a52-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2a52-133">OUTPUTS</span></span>

### <span data-ttu-id="f2a52-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="f2a52-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="f2a52-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2a52-135">NOTES</span></span>

## <span data-ttu-id="f2a52-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2a52-136">RELATED LINKS</span></span>
