---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8344d9e794189d67a69c1be9a88e135b721a0d4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542359"
---
# <span data-ttu-id="1945d-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1945d-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="1945d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1945d-102">SYNOPSIS</span></span>
<span data-ttu-id="1945d-103">Umożliwia filtrowanie podmiotów zabezpieczeń usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1945d-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1945d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1945d-104">SYNTAX</span></span>

### <span data-ttu-id="1945d-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1945d-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1945d-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1945d-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1945d-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1945d-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1945d-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="1945d-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1945d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1945d-109">DESCRIPTION</span></span>
<span data-ttu-id="1945d-110">Umożliwia filtrowanie podmiotów zabezpieczeń usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1945d-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="1945d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1945d-111">EXAMPLES</span></span>

### <span data-ttu-id="1945d-112">Filtruje podmioty zabezpieczeń usługi przy użyciu nazwy SPN</span><span class="sxs-lookup"><span data-stu-id="1945d-112">Filters service principals using SPN</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="1945d-113">Pobiera podmioty zabezpieczeń usługi przy użyciu 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span><span class="sxs-lookup"><span data-stu-id="1945d-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="1945d-114">Filtruje podmioty zabezpieczeń usługi przy użyciu ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="1945d-114">Filters service principals using Search String</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="1945d-115">Filtruje wszystkie podmioty zabezpieczeń usługi AD z wyświetlaną nazwą, rozpoczynając od "sieci Web".</span><span class="sxs-lookup"><span data-stu-id="1945d-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="1945d-116">Wyświetlanie podmiotów zabezpieczeń usługi AD</span><span class="sxs-lookup"><span data-stu-id="1945d-116">List AD service principals</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="1945d-117">Pobiera wszystkich głównych podmiotów usługi AD.</span><span class="sxs-lookup"><span data-stu-id="1945d-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="1945d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1945d-118">PARAMETERS</span></span>

### <span data-ttu-id="1945d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1945d-119">-DefaultProfile</span></span>
<span data-ttu-id="1945d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1945d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1945d-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1945d-121">-ObjectId</span></span>
<span data-ttu-id="1945d-122">Identyfikator obiektu głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="1945d-122">Object id of the service principal.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1945d-123">-SearchString</span><span class="sxs-lookup"><span data-stu-id="1945d-123">-SearchString</span></span>
<span data-ttu-id="1945d-124">Pobiera wszystkie podmioty główne usługi, których nazwa wyświetlana rozpoczyna się od tej wartości.</span><span class="sxs-lookup"><span data-stu-id="1945d-124">Fetches all service principals that have the display name starting with this value.</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1945d-125">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1945d-125">-ServicePrincipalName</span></span>
<span data-ttu-id="1945d-126">SPN usługi.</span><span class="sxs-lookup"><span data-stu-id="1945d-126">SPN of the service.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1945d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1945d-127">CommonParameters</span></span>
<span data-ttu-id="1945d-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1945d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1945d-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1945d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1945d-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1945d-130">INPUTS</span></span>

### <span data-ttu-id="1945d-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1945d-131">None</span></span>
<span data-ttu-id="1945d-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1945d-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1945d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1945d-133">OUTPUTS</span></span>

### <span data-ttu-id="1945d-134">System. Collections. Generic. list "1 [Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="1945d-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="1945d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1945d-135">NOTES</span></span>

## <span data-ttu-id="1945d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1945d-136">RELATED LINKS</span></span>

[<span data-ttu-id="1945d-137">Nowe — AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1945d-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="1945d-138">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1945d-138">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="1945d-139">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1945d-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="1945d-140">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1945d-140">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="1945d-141">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1945d-141">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

