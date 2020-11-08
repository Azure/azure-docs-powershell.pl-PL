---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 1e6358972e547e6a5fab54072396c3ad6fc7f418
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063489"
---
# <span data-ttu-id="61d28-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="61d28-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="61d28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61d28-102">SYNOPSIS</span></span>
<span data-ttu-id="61d28-103">Tworzy konto usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="61d28-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="61d28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61d28-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61d28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="61d28-105">DESCRIPTION</span></span>
<span data-ttu-id="61d28-106">Polecenie cmdlet New-AzMapsAccount powoduje utworzenie konta usługi Azure Maps przy użyciu określonej jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="61d28-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="61d28-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61d28-107">EXAMPLES</span></span>

### <span data-ttu-id="61d28-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="61d28-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="61d28-109">Tworzy nowe konto usługi Azure Maps o nazwie Moje konto w grupie zasoby moja grupa zasobów z S0ą SKU i znacznikiem.</span><span class="sxs-lookup"><span data-stu-id="61d28-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="61d28-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61d28-110">PARAMETERS</span></span>

### <span data-ttu-id="61d28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d28-111">-DefaultProfile</span></span>
<span data-ttu-id="61d28-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61d28-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61d28-113">-Force</span><span class="sxs-lookup"><span data-stu-id="61d28-113">-Force</span></span>
<span data-ttu-id="61d28-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="61d28-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="61d28-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61d28-115">-Name</span></span>
<span data-ttu-id="61d28-116">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="61d28-116">Maps Account Name.</span></span>

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

### <span data-ttu-id="61d28-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d28-117">-ResourceGroupName</span></span>
<span data-ttu-id="61d28-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61d28-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="61d28-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="61d28-119">-SkuName</span></span>
<span data-ttu-id="61d28-120">Mapowanie nazwy jednostki SKU konta.</span><span class="sxs-lookup"><span data-stu-id="61d28-120">Maps Account Sku Name.</span></span>

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

### <span data-ttu-id="61d28-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="61d28-121">-Tag</span></span>
<span data-ttu-id="61d28-122">Odwzorowuje znaczniki kont.</span><span class="sxs-lookup"><span data-stu-id="61d28-122">Maps Account Tags.</span></span>

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

### <span data-ttu-id="61d28-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61d28-123">-Confirm</span></span>
<span data-ttu-id="61d28-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61d28-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61d28-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61d28-125">-WhatIf</span></span>
<span data-ttu-id="61d28-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61d28-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61d28-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61d28-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61d28-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d28-128">CommonParameters</span></span>
<span data-ttu-id="61d28-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61d28-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d28-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61d28-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d28-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61d28-131">INPUTS</span></span>

### <span data-ttu-id="61d28-132">System. String</span><span class="sxs-lookup"><span data-stu-id="61d28-132">System.String</span></span>

## <span data-ttu-id="61d28-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61d28-133">OUTPUTS</span></span>

### <span data-ttu-id="61d28-134">Microsoft. Azure. Commands. Maps. modele. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="61d28-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="61d28-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61d28-135">NOTES</span></span>

## <span data-ttu-id="61d28-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61d28-136">RELATED LINKS</span></span>
