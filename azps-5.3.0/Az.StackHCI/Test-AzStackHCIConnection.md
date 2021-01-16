---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374255"
---
# <span data-ttu-id="abd56-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="abd56-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="abd56-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="abd56-102">SYNOPSIS</span></span>
<span data-ttu-id="abd56-103">Test-AzStackHCIConnection weryfikuje łączność z lokalnych węzłów klastrowanych z usługami platformy Azure wymaganymi przez stos HCL stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="abd56-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="abd56-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="abd56-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="abd56-105">Opis</span><span class="sxs-lookup"><span data-stu-id="abd56-105">DESCRIPTION</span></span>
<span data-ttu-id="abd56-106">Test-AzStackHCIConnection weryfikuje łączność z lokalnych węzłów klastrowanych z usługami platformy Azure wymaganymi przez stos HCL stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="abd56-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="abd56-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="abd56-107">EXAMPLES</span></span>

### <span data-ttu-id="abd56-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="abd56-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node. Success case.
```

<span data-ttu-id="abd56-109">Test C:\PS \> -AzStackHCIConnection: Nawiązywanie połączenia z usługą Azure Stack HCL EndpointTested: https://azurestackhci-df.azurefd.net/health isrequireded: prawda wyniku: powodzenie</span><span class="sxs-lookup"><span data-stu-id="abd56-109">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeeded</span></span>

### <span data-ttu-id="abd56-110">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="abd56-110">EXAMPLE 2</span></span>
```
Invoking on one of the cluster node. Failed case.
```

<span data-ttu-id="abd56-111">Test C:\PS \> -AzStackHCIConnection: Nawiązywanie połączenia z usługą Azure Stack HCL EndpointTested: https://azurestackhci-df.azurefd.net/health isrequireded: prawda wyniku: niepowodzenie FailedNodes: Node1inClus2, Node2inClus3</span><span class="sxs-lookup"><span data-stu-id="abd56-111">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3</span></span>

## <span data-ttu-id="abd56-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="abd56-112">PARAMETERS</span></span>

### <span data-ttu-id="abd56-113">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="abd56-113">-ComputerName</span></span>
<span data-ttu-id="abd56-114">Umożliwia określenie jednego węzła klastra w klastrze lokalnym, który jest rejestrowany na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="abd56-114">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="abd56-115">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="abd56-115">-Credential</span></span>
<span data-ttu-id="abd56-116">Określa poświadczenie dla komputera ComputerName.</span><span class="sxs-lookup"><span data-stu-id="abd56-116">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="abd56-117">Domyślnie jest to bieżący użytkownik wykonujący polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abd56-117">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="abd56-118">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="abd56-118">-EnvironmentName</span></span>
<span data-ttu-id="abd56-119">Określa środowisko Azure.</span><span class="sxs-lookup"><span data-stu-id="abd56-119">Specifies the Azure Environment.</span></span>
<span data-ttu-id="abd56-120">Domyślna to AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="abd56-120">Default is AzureCloud.</span></span>
<span data-ttu-id="abd56-121">Prawidłowe wartości to AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="abd56-121">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="abd56-122">-Region</span><span class="sxs-lookup"><span data-stu-id="abd56-122">-Region</span></span>
<span data-ttu-id="abd56-123">Określa region, z którym ma zostać nawiązane połączenie.</span><span class="sxs-lookup"><span data-stu-id="abd56-123">Specifies the Region to connect to.</span></span>
<span data-ttu-id="abd56-124">Nieużywane, chyba że jest to region Kanaryjskie.</span><span class="sxs-lookup"><span data-stu-id="abd56-124">Not used unless it is Canary region.</span></span>

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

### <span data-ttu-id="abd56-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd56-125">CommonParameters</span></span>
<span data-ttu-id="abd56-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abd56-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd56-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abd56-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd56-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abd56-128">INPUTS</span></span>

## <span data-ttu-id="abd56-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="abd56-129">OUTPUTS</span></span>

### <span data-ttu-id="abd56-130">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="abd56-130">PSCustomObject.</span></span> <span data-ttu-id="abd56-131">Zwraca następujące właściwości w PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="abd56-131">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="abd56-132">Test: Nazwa przeprowadzonego testu.</span><span class="sxs-lookup"><span data-stu-id="abd56-132">Test: Name of the test performed.</span></span>
### <span data-ttu-id="abd56-133">EndpointTested: punkt końcowy stosowany w teście.</span><span class="sxs-lookup"><span data-stu-id="abd56-133">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="abd56-134">IsRequired: prawda lub FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="abd56-134">IsRequired: True or False</span></span>
### <span data-ttu-id="abd56-135">Wynik: powodzenie lub niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="abd56-135">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="abd56-136">FailedNodes: lista węzłów, których test nie powiódł się.</span><span class="sxs-lookup"><span data-stu-id="abd56-136">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="abd56-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="abd56-137">NOTES</span></span>

## <span data-ttu-id="abd56-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abd56-138">RELATED LINKS</span></span>
