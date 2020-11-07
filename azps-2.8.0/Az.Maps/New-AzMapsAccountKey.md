---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: 68a03059a99c8e50d5f0ae77b131fa8ab9ed6d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704881"
---
# <span data-ttu-id="d4905-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="d4905-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="d4905-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4905-102">SYNOPSIS</span></span>
<span data-ttu-id="d4905-103">Generuje ponownie klucz konta.</span><span class="sxs-lookup"><span data-stu-id="d4905-103">Regenerates an account key.</span></span>

## <span data-ttu-id="d4905-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4905-104">SYNTAX</span></span>

### <span data-ttu-id="d4905-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d4905-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4905-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4905-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4905-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4905-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4905-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d4905-108">DESCRIPTION</span></span>
<span data-ttu-id="d4905-109">Polecenie cmdlet New-AzMapsAccountKey ponownie generuje klucz interfejsu API dla konta usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="d4905-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="d4905-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4905-110">EXAMPLES</span></span>

### <span data-ttu-id="d4905-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d4905-111">Example 1</span></span>
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

<span data-ttu-id="d4905-112">Generuje ponownie podstawowy klucz interfejsu API dla konta Moje konto w grupie zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4905-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="d4905-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d4905-113">Example 2</span></span>
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

<span data-ttu-id="d4905-114">Generuje ponownie pomocniczy klucz API dla określonego konta usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="d4905-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="d4905-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4905-115">PARAMETERS</span></span>

### <span data-ttu-id="d4905-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4905-116">-DefaultProfile</span></span>
<span data-ttu-id="d4905-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4905-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4905-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4905-118">-InputObject</span></span>
<span data-ttu-id="d4905-119">Konto mapy potoku w usłudze Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="d4905-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="d4905-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="d4905-120">-KeyName</span></span>
<span data-ttu-id="d4905-121">Mapowanie klucza konta.</span><span class="sxs-lookup"><span data-stu-id="d4905-121">Maps Account Key.</span></span>

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

### <span data-ttu-id="d4905-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4905-122">-Name</span></span>
<span data-ttu-id="d4905-123">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="d4905-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="d4905-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4905-124">-ResourceGroupName</span></span>
<span data-ttu-id="d4905-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4905-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d4905-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4905-126">-ResourceId</span></span>
<span data-ttu-id="d4905-127">Mapowanie ResourceId konta.</span><span class="sxs-lookup"><span data-stu-id="d4905-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="d4905-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4905-128">-Confirm</span></span>
<span data-ttu-id="d4905-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4905-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4905-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4905-130">-WhatIf</span></span>
<span data-ttu-id="d4905-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4905-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4905-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4905-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4905-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4905-133">CommonParameters</span></span>
<span data-ttu-id="d4905-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4905-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4905-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4905-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4905-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4905-136">INPUTS</span></span>

### <span data-ttu-id="d4905-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d4905-137">System.String</span></span>

### <span data-ttu-id="d4905-138">Microsoft. Azure. Commands. Maps. modele. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="d4905-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="d4905-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4905-139">OUTPUTS</span></span>

### <span data-ttu-id="d4905-140">Microsoft. Azure. Management. Maps. modele. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d4905-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="d4905-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4905-141">NOTES</span></span>

## <span data-ttu-id="d4905-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4905-142">RELATED LINKS</span></span>