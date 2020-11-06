---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 34f4b85a299e714f524b1a4d33f2fb717483c377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553116"
---
# <span data-ttu-id="dff5a-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dff5a-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="dff5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dff5a-102">SYNOPSIS</span></span>
<span data-ttu-id="dff5a-103">Umożliwia filtrowanie podmiotów zabezpieczeń usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dff5a-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dff5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dff5a-104">SYNTAX</span></span>

### <span data-ttu-id="dff5a-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dff5a-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dff5a-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dff5a-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dff5a-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dff5a-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dff5a-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dff5a-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dff5a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="dff5a-109">DESCRIPTION</span></span>
<span data-ttu-id="dff5a-110">Umożliwia filtrowanie podmiotów zabezpieczeń usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dff5a-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="dff5a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dff5a-111">EXAMPLES</span></span>

### <span data-ttu-id="dff5a-112">--------------------------Filtruje podmioty zabezpieczeń usługi przy użyciu nazwy SPN--------------------------</span><span class="sxs-lookup"><span data-stu-id="dff5a-112">--------------------------  Filters service principals using SPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="dff5a-113">Pobiera podmioty zabezpieczeń usługi przy użyciu 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span><span class="sxs-lookup"><span data-stu-id="dff5a-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="dff5a-114">--------------------------Filtruje podmioty zabezpieczeń usługi przy użyciu ciągu wyszukiwania--------------------------</span><span class="sxs-lookup"><span data-stu-id="dff5a-114">--------------------------  Filters service principals using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="dff5a-115">Filtruje wszystkie podmioty zabezpieczeń usługi AD z wyświetlaną nazwą, rozpoczynając od "sieci Web".</span><span class="sxs-lookup"><span data-stu-id="dff5a-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="dff5a-116">----------------------------------------------------Głównych usług REKLAMowych</span><span class="sxs-lookup"><span data-stu-id="dff5a-116">--------------------------  List AD service principals  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="dff5a-117">Pobiera wszystkich głównych podmiotów usługi AD.</span><span class="sxs-lookup"><span data-stu-id="dff5a-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="dff5a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dff5a-118">PARAMETERS</span></span>

### <span data-ttu-id="dff5a-119">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dff5a-119">-ObjectId</span></span>
<span data-ttu-id="dff5a-120">Identyfikator obiektu głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="dff5a-120">Object id of the service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dff5a-121">-SearchString</span><span class="sxs-lookup"><span data-stu-id="dff5a-121">-SearchString</span></span>
<span data-ttu-id="dff5a-122">Pobiera wszystkie podmioty główne usługi, których nazwa wyświetlana rozpoczyna się od tej wartości.</span><span class="sxs-lookup"><span data-stu-id="dff5a-122">Fetches all service principals that have the display name starting with this value.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dff5a-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dff5a-123">-ServicePrincipalName</span></span>
<span data-ttu-id="dff5a-124">SPN usługi.</span><span class="sxs-lookup"><span data-stu-id="dff5a-124">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: SPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dff5a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff5a-125">-DefaultProfile</span></span>
<span data-ttu-id="dff5a-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dff5a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dff5a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff5a-127">CommonParameters</span></span>
<span data-ttu-id="dff5a-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dff5a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff5a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dff5a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff5a-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dff5a-130">INPUTS</span></span>

## <span data-ttu-id="dff5a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dff5a-131">OUTPUTS</span></span>

### <span data-ttu-id="dff5a-132">System. Collections. Generic. list "1 [Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="dff5a-132">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="dff5a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dff5a-133">NOTES</span></span>

## <span data-ttu-id="dff5a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dff5a-134">RELATED LINKS</span></span>

[<span data-ttu-id="dff5a-135">Nowe — AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dff5a-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="dff5a-136">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dff5a-136">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="dff5a-137">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dff5a-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="dff5a-138">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="dff5a-138">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="dff5a-139">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="dff5a-139">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

