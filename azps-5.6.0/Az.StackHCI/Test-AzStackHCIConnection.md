---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 4de1e1467e1bc422666b7144f5d5fcd6c30c0c63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976209"
---
# <span data-ttu-id="65a3c-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="65a3c-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="65a3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="65a3c-103">Test-AzStackHCIConnection sprawdza łączność lokalnych węzłów grupowanych z usługami Azure wymaganymi przez usługę Azure Stack HCI.</span><span class="sxs-lookup"><span data-stu-id="65a3c-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="65a3c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="65a3c-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="65a3c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="65a3c-105">DESCRIPTION</span></span>
<span data-ttu-id="65a3c-106">Test-AzStackHCIConnection sprawdza łączność lokalnych węzłów grupowanych z usługami Azure wymaganymi przez usługę Azure Stack HCI.</span><span class="sxs-lookup"><span data-stu-id="65a3c-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="65a3c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="65a3c-107">EXAMPLES</span></span>

### <span data-ttu-id="65a3c-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="65a3c-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
<span data-ttu-id="65a3c-109">Wywołuj w jednym z węźle klastrów.</span><span class="sxs-lookup"><span data-stu-id="65a3c-109">Invoking on one of the cluster node.</span></span> <span data-ttu-id="65a3c-110">Przypadek sukcesu.</span><span class="sxs-lookup"><span data-stu-id="65a3c-110">Success case.</span></span>

### <span data-ttu-id="65a3c-111">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="65a3c-111">EXAMPLE 2</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
<span data-ttu-id="65a3c-112">Wywołuj w jednym z węźle klastrów.</span><span class="sxs-lookup"><span data-stu-id="65a3c-112">Invoking on one of the cluster node.</span></span> <span data-ttu-id="65a3c-113">Nie powiodła się sprawa.</span><span class="sxs-lookup"><span data-stu-id="65a3c-113">Failed case.</span></span>

## <span data-ttu-id="65a3c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65a3c-114">PARAMETERS</span></span>

### <span data-ttu-id="65a3c-115">— Nazwa_komputera</span><span class="sxs-lookup"><span data-stu-id="65a3c-115">-ComputerName</span></span>
<span data-ttu-id="65a3c-116">Określa jeden z węzła klastrów w klastrze lokalnym, który jest zarejestrowany na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="65a3c-116">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a3c-117">- Credential</span><span class="sxs-lookup"><span data-stu-id="65a3c-117">-Credential</span></span>
<span data-ttu-id="65a3c-118">Określa poświadczenia dla parametru Nazwa_komputera.</span><span class="sxs-lookup"><span data-stu-id="65a3c-118">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="65a3c-119">Wartość domyślna to bieżący użytkownik wykonujący polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a3c-119">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a3c-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="65a3c-120">-EnvironmentName</span></span>
<span data-ttu-id="65a3c-121">Określa środowisko platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="65a3c-121">Specifies the Azure Environment.</span></span>
<span data-ttu-id="65a3c-122">Wartością domyślną jest usługa AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="65a3c-122">Default is AzureCloud.</span></span>
<span data-ttu-id="65a3c-123">Prawidłowe wartości to: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="65a3c-123">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a3c-124">— Region</span><span class="sxs-lookup"><span data-stu-id="65a3c-124">-Region</span></span>
<span data-ttu-id="65a3c-125">Określa region, z który ma nawiązać połączenie.</span><span class="sxs-lookup"><span data-stu-id="65a3c-125">Specifies the Region to connect to.</span></span>
<span data-ttu-id="65a3c-126">Nie jest używany, chyba że jest to region Canary.</span><span class="sxs-lookup"><span data-stu-id="65a3c-126">Not used unless it is Canary region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a3c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a3c-127">CommonParameters</span></span>
<span data-ttu-id="65a3c-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a3c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a3c-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65a3c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a3c-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65a3c-130">INPUTS</span></span>

## <span data-ttu-id="65a3c-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65a3c-131">OUTPUTS</span></span>

### <span data-ttu-id="65a3c-132">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="65a3c-132">PSCustomObject.</span></span> <span data-ttu-id="65a3c-133">Zwraca następujące właściwości w programie PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="65a3c-133">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="65a3c-134">Test: nazwa wykonanego testu.</span><span class="sxs-lookup"><span data-stu-id="65a3c-134">Test: Name of the test performed.</span></span>
### <span data-ttu-id="65a3c-135">EndpointTested: Punkt końcowy używany w teście.</span><span class="sxs-lookup"><span data-stu-id="65a3c-135">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="65a3c-136">IsRequired: True or False</span><span class="sxs-lookup"><span data-stu-id="65a3c-136">IsRequired: True or False</span></span>
### <span data-ttu-id="65a3c-137">Wynik: powodzenie lub niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="65a3c-137">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="65a3c-138">FailedNodes: lista węzłów, w których test zakończył się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="65a3c-138">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="65a3c-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="65a3c-139">NOTES</span></span>

## <span data-ttu-id="65a3c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65a3c-140">RELATED LINKS</span></span>
