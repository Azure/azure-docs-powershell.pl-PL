---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
ms.openlocfilehash: 1afe0f8f93bd00a384e1bb741ed8ea54e1ae66d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546511"
---
# <span data-ttu-id="29289-101">Get-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="29289-101">Get-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="29289-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29289-102">SYNOPSIS</span></span>
<span data-ttu-id="29289-103">Pobiera klucze interfejsu API dla konta.</span><span class="sxs-lookup"><span data-stu-id="29289-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="29289-104">Te klucze są mechanizmem uwierzytelniania stosowanym w kolejnych połączeniach z usługą Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="29289-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29289-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29289-105">SYNTAX</span></span>

### <span data-ttu-id="29289-106">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="29289-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29289-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29289-107">InputObjectParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29289-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29289-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29289-109">Opis</span><span class="sxs-lookup"><span data-stu-id="29289-109">DESCRIPTION</span></span>
<span data-ttu-id="29289-110">Polecenie cmdlet Get-AzureRmMapsAccountKey pobiera klucze interfejsu API dla konta usługi Azure Maps z obsługą administracyjną.</span><span class="sxs-lookup"><span data-stu-id="29289-110">The Get-AzureRmMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="29289-111">Konto usługi Azure Maps ma dwa klucze API: podstawowy i pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="29289-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="29289-112">Klucze umożliwiają interakcję z punktem końcowym konta usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="29289-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="29289-113">Aby ponownie wygenerować klucz, użyj New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey. MD).</span><span class="sxs-lookup"><span data-stu-id="29289-113">Use New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="29289-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29289-114">EXAMPLES</span></span>

### <span data-ttu-id="29289-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="29289-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="29289-116">Zwraca klucze konta o nazwie Moje konto w grupie zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="29289-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="29289-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="29289-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="29289-118">Zwraca klucze określonego konta usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="29289-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="29289-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29289-119">PARAMETERS</span></span>

### <span data-ttu-id="29289-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29289-120">-DefaultProfile</span></span>
<span data-ttu-id="29289-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29289-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29289-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="29289-122">-InputObject</span></span>
<span data-ttu-id="29289-123">Konto mapy potoku w usłudze Get-AzureRmMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="29289-123">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

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

### <span data-ttu-id="29289-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29289-124">-Name</span></span>
<span data-ttu-id="29289-125">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="29289-125">Maps Account Name.</span></span>

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

### <span data-ttu-id="29289-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29289-126">-ResourceGroupName</span></span>
<span data-ttu-id="29289-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="29289-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="29289-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29289-128">-ResourceId</span></span>
<span data-ttu-id="29289-129">Mapowanie ResourceId konta.</span><span class="sxs-lookup"><span data-stu-id="29289-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="29289-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29289-130">CommonParameters</span></span>
<span data-ttu-id="29289-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29289-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29289-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29289-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29289-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29289-133">INPUTS</span></span>

### <span data-ttu-id="29289-134">System. String</span><span class="sxs-lookup"><span data-stu-id="29289-134">System.String</span></span>

### <span data-ttu-id="29289-135">Microsoft. Azure. Commands. Maps. modele. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="29289-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="29289-136">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="29289-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="29289-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29289-137">OUTPUTS</span></span>

### <span data-ttu-id="29289-138">Microsoft. Azure. Commands. Maps. modele. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="29289-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="29289-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29289-139">NOTES</span></span>

## <span data-ttu-id="29289-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29289-140">RELATED LINKS</span></span>
