---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 7116cd4c5da2dd897af4e6540593a5e5458e4eda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544275"
---
# <span data-ttu-id="b3ce1-101">New-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="b3ce1-101">New-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="b3ce1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ce1-103">Generuje ponownie klucz konta.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3ce1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3ce1-104">SYNTAX</span></span>

### <span data-ttu-id="b3ce1-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3ce1-105">NameParameterSet (Default)</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3ce1-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3ce1-106">InputObjectParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3ce1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3ce1-107">ResourceIdParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3ce1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b3ce1-108">DESCRIPTION</span></span>
<span data-ttu-id="b3ce1-109">Polecenie cmdlet **New-AzureRmLocationBasedServicesAccountKey** GENERUJE klucz API dla konta usług opartego na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-109">The **New-AzureRmLocationBasedServicesAccountKey** cmdlet regenerates an API key for a Location Based Services account.</span></span>

## <span data-ttu-id="b3ce1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3ce1-110">EXAMPLES</span></span>

### <span data-ttu-id="b3ce1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3ce1-111">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="b3ce1-112">Generuje ponownie podstawowy klucz interfejsu API dla konta Moje konto w grupie zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="b3ce1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b3ce1-113">Example 2</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="b3ce1-114">Ponownie generuje pomocniczy klucz API dla określonego konta usługi opartego na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-114">Regenerates the Secondary API Key for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="b3ce1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3ce1-115">PARAMETERS</span></span>

### <span data-ttu-id="b3ce1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ce1-116">-DefaultProfile</span></span>
<span data-ttu-id="b3ce1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce1-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3ce1-118">-InputObject</span></span>
<span data-ttu-id="b3ce1-119">Konto usług opartych na lokalizacji potoku w usłudze [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="b3ce1-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce1-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="b3ce1-120">-KeyName</span></span>
<span data-ttu-id="b3ce1-121">Klucz konta usług opartych na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-121">Location Based Services Account Key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce1-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3ce1-122">-Name</span></span>
<span data-ttu-id="b3ce1-123">Nazwa konta usług opartych na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-123">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3ce1-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3ce1-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3ce1-126">-ResourceId</span></span>
<span data-ttu-id="b3ce1-127">Identyfikator ResourceId konta usług opartych na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-127">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce1-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3ce1-128">-Confirm</span></span>
<span data-ttu-id="b3ce1-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3ce1-130">-WhatIf</span></span>
<span data-ttu-id="b3ce1-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3ce1-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ce1-133">CommonParameters</span></span>
<span data-ttu-id="b3ce1-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3ce1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ce1-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3ce1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ce1-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3ce1-136">INPUTS</span></span>

### <span data-ttu-id="b3ce1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b3ce1-137">System.String</span></span>
<span data-ttu-id="b3ce1-138">Microsoft. Azure. Commands. LocationBasedServices. NewAzureLocationBasedServicesAccountKeyCommand + nameType</span><span class="sxs-lookup"><span data-stu-id="b3ce1-138">Microsoft.Azure.Commands.LocationBasedServices.NewAzureLocationBasedServicesAccountKeyCommand+KeyNameType</span></span>

## <span data-ttu-id="b3ce1-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3ce1-139">OUTPUTS</span></span>

### <span data-ttu-id="b3ce1-140">Microsoft. Azure. Management. LocationBasedServices. MODELES. LocationBasedServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b3ce1-140">Microsoft.Azure.Management.LocationBasedServices.Models.LocationBasedServicesAccountKeys</span></span>

## <span data-ttu-id="b3ce1-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3ce1-141">NOTES</span></span>

## <span data-ttu-id="b3ce1-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3ce1-142">RELATED LINKS</span></span>
