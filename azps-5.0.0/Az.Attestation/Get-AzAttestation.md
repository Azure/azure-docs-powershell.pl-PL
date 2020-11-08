---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225107"
---
# <span data-ttu-id="b27b9-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="b27b9-101">Get-AzAttestation</span></span>

## <span data-ttu-id="b27b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b27b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b27b9-103">Pobiera zaświadczenie.</span><span class="sxs-lookup"><span data-stu-id="b27b9-103">Gets an attestation.</span></span>

## <span data-ttu-id="b27b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b27b9-104">SYNTAX</span></span>

### <span data-ttu-id="b27b9-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b27b9-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b27b9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b27b9-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b27b9-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="b27b9-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b27b9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b27b9-108">DESCRIPTION</span></span>
<span data-ttu-id="b27b9-109">Polecenie cmdlet Get-AzAttestation pobiera informacje o zaświadczeniu w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="b27b9-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="b27b9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b27b9-110">EXAMPLES</span></span>

### <span data-ttu-id="b27b9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b27b9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                                       
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest.us.attest.azure.net
Tags              : {Production, Example}
TagsTable         :
                    Name        Value
                    ==========  =====
                    Production  False
                    Example     True
```

<span data-ttu-id="b27b9-112">Pobierz *Pshtest* dostawcy zaświadczania w grupie zasób *PSH-test-RG*.</span><span class="sxs-lookup"><span data-stu-id="b27b9-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="b27b9-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b27b9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/sharedcus
Location          : Central US
ResourceGroupName :
Name              : sharedcus
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedcus.cus.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/shareduks
Location          : UK South
ResourceGroupName :
Name              : shareduks
Status            : Ready
TrustModel        : AAD
AttestUri         : https://shareduks.uks.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="b27b9-114">Uzyskaj wszystkich dostępnych dostawców domyślnych zaświadczania</span><span class="sxs-lookup"><span data-stu-id="b27b9-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="b27b9-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b27b9-115">Example 3</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider -Location "East US 2"
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="b27b9-116">Uzyskaj domyślnego dostawcę zaświadczania z lokalizacji *wschód USA 2*</span><span class="sxs-lookup"><span data-stu-id="b27b9-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="b27b9-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b27b9-117">PARAMETERS</span></span>

### <span data-ttu-id="b27b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27b9-118">-DefaultProfile</span></span>
<span data-ttu-id="b27b9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b27b9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b27b9-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="b27b9-120">-DefaultProvider</span></span>
<span data-ttu-id="b27b9-121">Określa, że jest to żądanie do domyślnego dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="b27b9-121">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b27b9-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b27b9-122">-Location</span></span>
<span data-ttu-id="b27b9-123">Określa lokalizację domyślnego dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="b27b9-123">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b27b9-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b27b9-124">-Name</span></span>
<span data-ttu-id="b27b9-125">Nazwa zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="b27b9-125">Attestation Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27b9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b27b9-126">-ResourceGroupName</span></span>
<span data-ttu-id="b27b9-127">Określa nazwę grupy zasobów skojarzonej z poszukiwanym zaświadczeniem.</span><span class="sxs-lookup"><span data-stu-id="b27b9-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27b9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b27b9-128">-ResourceId</span></span>
<span data-ttu-id="b27b9-129">Określa nazwę ResourceID skojarzonego z poszukiwanym zaświadczeniem</span><span class="sxs-lookup"><span data-stu-id="b27b9-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="b27b9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27b9-130">CommonParameters</span></span>
<span data-ttu-id="b27b9-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b27b9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27b9-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b27b9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27b9-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b27b9-133">INPUTS</span></span>

### <span data-ttu-id="b27b9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b27b9-134">System.String</span></span>

## <span data-ttu-id="b27b9-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b27b9-135">OUTPUTS</span></span>

### <span data-ttu-id="b27b9-136">Microsoft. Azure. Commands. zaświadczanie. modele. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="b27b9-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="b27b9-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b27b9-137">NOTES</span></span>

## <span data-ttu-id="b27b9-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b27b9-138">RELATED LINKS</span></span>
