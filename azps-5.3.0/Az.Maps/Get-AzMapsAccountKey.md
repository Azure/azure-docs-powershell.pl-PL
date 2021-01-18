---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: 4969ba5cdb8b24627e620b82a13806c7b4cc687e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499721"
---
# <span data-ttu-id="7c7f3-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="7c7f3-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="7c7f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c7f3-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7f3-103">Pobiera klucze interfejsu API dla konta.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="7c7f3-104">Te klucze są mechanizmem uwierzytelniania stosowanym w kolejnych połączeniach z usługą Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="7c7f3-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c7f3-105">SYNTAX</span></span>

### <span data-ttu-id="7c7f3-106">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7c7f3-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c7f3-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c7f3-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c7f3-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c7f3-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c7f3-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7c7f3-109">DESCRIPTION</span></span>
<span data-ttu-id="7c7f3-110">Polecenie cmdlet Get-AzMapsAccountKey pobiera klucze interfejsu API dla konta usługi Azure Maps z obsługą administracyjną.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="7c7f3-111">Konto usługi Azure Maps ma dwa klucze API: podstawowy i pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="7c7f3-112">Klucze umożliwiają interakcję z punktem końcowym konta usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="7c7f3-113">Aby ponownie wygenerować klucz, użyj New-AzMapsAccountKey (New-AzMapsAccountKey. MD).</span><span class="sxs-lookup"><span data-stu-id="7c7f3-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="7c7f3-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c7f3-114">EXAMPLES</span></span>

### <span data-ttu-id="7c7f3-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7c7f3-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="7c7f3-116">Zwraca klucze konta o nazwie Moje konto w grupie zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="7c7f3-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7c7f3-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="7c7f3-118">Zwraca klucze określonego konta usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="7c7f3-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c7f3-119">PARAMETERS</span></span>

### <span data-ttu-id="7c7f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c7f3-120">-DefaultProfile</span></span>
<span data-ttu-id="7c7f3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c7f3-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7c7f3-122">-InputObject</span></span>
<span data-ttu-id="7c7f3-123">Konto mapy potoku w usłudze Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-123">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="7c7f3-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7c7f3-124">-Name</span></span>
<span data-ttu-id="7c7f3-125">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-125">Maps Account Name.</span></span>

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

### <span data-ttu-id="7c7f3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c7f3-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c7f3-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="7c7f3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c7f3-128">-ResourceId</span></span>
<span data-ttu-id="7c7f3-129">Mapowanie ResourceId konta.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="7c7f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7f3-130">CommonParameters</span></span>
<span data-ttu-id="7c7f3-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7f3-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c7f3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7f3-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c7f3-133">INPUTS</span></span>

### <span data-ttu-id="7c7f3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7c7f3-134">System.String</span></span>

### <span data-ttu-id="7c7f3-135">Microsoft. Azure. Commands. Maps. modele. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="7c7f3-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="7c7f3-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c7f3-136">OUTPUTS</span></span>

### <span data-ttu-id="7c7f3-137">Microsoft. Azure. Commands. Maps. modele. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7c7f3-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="7c7f3-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c7f3-138">NOTES</span></span>

## <span data-ttu-id="7c7f3-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c7f3-139">RELATED LINKS</span></span>
