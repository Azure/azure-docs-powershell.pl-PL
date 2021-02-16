---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: c115cd780750770e05bc55b1f70a7cfe33967fff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241275"
---
# <span data-ttu-id="cf19a-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="cf19a-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="cf19a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf19a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf19a-103">Ponownie generuje klucz konta.</span><span class="sxs-lookup"><span data-stu-id="cf19a-103">Regenerates an account key.</span></span>

## <span data-ttu-id="cf19a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf19a-104">SYNTAX</span></span>

### <span data-ttu-id="cf19a-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="cf19a-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf19a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf19a-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf19a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf19a-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf19a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf19a-108">DESCRIPTION</span></span>
<span data-ttu-id="cf19a-109">Polecenie New-AzMapsAccountKey ponownie generuje klucz interfejsu API dla konta usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="cf19a-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="cf19a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf19a-110">EXAMPLES</span></span>

### <span data-ttu-id="cf19a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cf19a-111">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="cf19a-112">Ponownie generuje podstawowy klucz interfejsu API dla konta MyAccount w grupie zasobów MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cf19a-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="cf19a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cf19a-113">Example 2</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="cf19a-114">Ponowne generowanie pomocniczego klucza interfejsu API dla określonego konta usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="cf19a-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="cf19a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf19a-115">PARAMETERS</span></span>

### <span data-ttu-id="cf19a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf19a-116">-DefaultProfile</span></span>
<span data-ttu-id="cf19a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf19a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf19a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf19a-118">-InputObject</span></span>
<span data-ttu-id="cf19a-119">Konto mapy potokowo z Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="cf19a-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf19a-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="cf19a-120">-KeyName</span></span>
<span data-ttu-id="cf19a-121">Klucz konta mapy.</span><span class="sxs-lookup"><span data-stu-id="cf19a-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf19a-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cf19a-122">-Name</span></span>
<span data-ttu-id="cf19a-123">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="cf19a-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf19a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf19a-124">-ResourceGroupName</span></span>
<span data-ttu-id="cf19a-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf19a-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf19a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf19a-126">-ResourceId</span></span>
<span data-ttu-id="cf19a-127">Konto mapy ResourceId.</span><span class="sxs-lookup"><span data-stu-id="cf19a-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf19a-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf19a-128">-Confirm</span></span>
<span data-ttu-id="cf19a-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cf19a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf19a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf19a-130">-WhatIf</span></span>
<span data-ttu-id="cf19a-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf19a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf19a-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cf19a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf19a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf19a-133">CommonParameters</span></span>
<span data-ttu-id="cf19a-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf19a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf19a-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf19a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf19a-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf19a-136">INPUTS</span></span>

### <span data-ttu-id="cf19a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="cf19a-137">System.String</span></span>

### <span data-ttu-id="cf19a-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="cf19a-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="cf19a-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf19a-139">OUTPUTS</span></span>

### <span data-ttu-id="cf19a-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cf19a-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="cf19a-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf19a-141">NOTES</span></span>

## <span data-ttu-id="cf19a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf19a-142">RELATED LINKS</span></span>
