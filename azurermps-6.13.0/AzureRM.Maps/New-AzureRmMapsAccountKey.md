---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
ms.openlocfilehash: 13364cde6799a6d99bcdba1d5cd2078c3392a2cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546504"
---
# <span data-ttu-id="789cf-101">New-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="789cf-101">New-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="789cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="789cf-102">SYNOPSIS</span></span>
<span data-ttu-id="789cf-103">Generuje ponownie klucz konta.</span><span class="sxs-lookup"><span data-stu-id="789cf-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="789cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="789cf-104">SYNTAX</span></span>

### <span data-ttu-id="789cf-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="789cf-105">NameParameterSet (Default)</span></span>
```
New-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="789cf-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="789cf-106">InputObjectParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="789cf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="789cf-107">ResourceIdParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="789cf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="789cf-108">DESCRIPTION</span></span>
<span data-ttu-id="789cf-109">Polecenie cmdlet New-AzureRmMapsAccountKey ponownie generuje klucz interfejsu API dla konta usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="789cf-109">The New-AzureRmMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="789cf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="789cf-110">EXAMPLES</span></span>

### <span data-ttu-id="789cf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="789cf-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="789cf-112">Generuje ponownie podstawowy klucz interfejsu API dla konta Moje konto w grupie zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="789cf-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="789cf-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="789cf-113">Example 2</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="789cf-114">Generuje ponownie pomocniczy klucz API dla określonego konta usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="789cf-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="789cf-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="789cf-115">PARAMETERS</span></span>

### <span data-ttu-id="789cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789cf-116">-DefaultProfile</span></span>
<span data-ttu-id="789cf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="789cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="789cf-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="789cf-118">-InputObject</span></span>
<span data-ttu-id="789cf-119">Konto mapy potoku w usłudze Get-AzureRmMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="789cf-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

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

### <span data-ttu-id="789cf-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="789cf-120">-KeyName</span></span>
<span data-ttu-id="789cf-121">Mapowanie klucza konta.</span><span class="sxs-lookup"><span data-stu-id="789cf-121">Maps Account Key.</span></span>

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

### <span data-ttu-id="789cf-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="789cf-122">-Name</span></span>
<span data-ttu-id="789cf-123">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="789cf-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="789cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="789cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="789cf-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="789cf-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="789cf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="789cf-126">-ResourceId</span></span>
<span data-ttu-id="789cf-127">Mapowanie ResourceId konta.</span><span class="sxs-lookup"><span data-stu-id="789cf-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="789cf-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="789cf-128">-Confirm</span></span>
<span data-ttu-id="789cf-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="789cf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="789cf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="789cf-130">-WhatIf</span></span>
<span data-ttu-id="789cf-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="789cf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="789cf-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="789cf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="789cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789cf-133">CommonParameters</span></span>
<span data-ttu-id="789cf-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="789cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789cf-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="789cf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789cf-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="789cf-136">INPUTS</span></span>

### <span data-ttu-id="789cf-137">System. String</span><span class="sxs-lookup"><span data-stu-id="789cf-137">System.String</span></span>

### <span data-ttu-id="789cf-138">Microsoft. Azure. Commands. Maps. modele. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="789cf-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="789cf-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="789cf-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="789cf-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="789cf-140">OUTPUTS</span></span>

### <span data-ttu-id="789cf-141">Microsoft. Azure. Management. Maps. modele. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="789cf-141">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="789cf-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="789cf-142">NOTES</span></span>

## <span data-ttu-id="789cf-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="789cf-143">RELATED LINKS</span></span>
