---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199690"
---
# <span data-ttu-id="18a79-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="18a79-101">Get-AzAttestation</span></span>

## <span data-ttu-id="18a79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18a79-102">SYNOPSIS</span></span>
<span data-ttu-id="18a79-103">Otrzymuje poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="18a79-103">Gets an attestation.</span></span>

## <span data-ttu-id="18a79-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="18a79-104">SYNTAX</span></span>

### <span data-ttu-id="18a79-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="18a79-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18a79-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18a79-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18a79-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="18a79-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18a79-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="18a79-108">DESCRIPTION</span></span>
<span data-ttu-id="18a79-109">Polecenie cmdlet Get-AzAttestation uzyskać informacje o atestacjach w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="18a79-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="18a79-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="18a79-110">EXAMPLES</span></span>

### <span data-ttu-id="18a79-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18a79-111">Example 1</span></span>
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

<span data-ttu-id="18a79-112">Pobierz test *pshtestu dostawcy atestacji* w grupie zasobów *psh-test-rg.*</span><span class="sxs-lookup"><span data-stu-id="18a79-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="18a79-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="18a79-113">Example 2</span></span>
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

<span data-ttu-id="18a79-114">Uzyskaj wszystkich dostępnych domyślnych dostawców poświadczenia</span><span class="sxs-lookup"><span data-stu-id="18a79-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="18a79-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="18a79-115">Example 3</span></span>
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

<span data-ttu-id="18a79-116">Uzyskaj domyślnego dostawcę usług Attestation z lokalizacji *Wschód Stanów Zjednoczonych 2*</span><span class="sxs-lookup"><span data-stu-id="18a79-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="18a79-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18a79-117">PARAMETERS</span></span>

### <span data-ttu-id="18a79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a79-118">-DefaultProfile</span></span>
<span data-ttu-id="18a79-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="18a79-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18a79-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="18a79-120">-DefaultProvider</span></span>
<span data-ttu-id="18a79-121">Określa to żądanie domyślnego dostawcy poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="18a79-121">Specifies this is the request to a default attestation provider.</span></span>

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

### <span data-ttu-id="18a79-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="18a79-122">-Location</span></span>
<span data-ttu-id="18a79-123">Określa lokalizację domyślnego dostawcy poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="18a79-123">Specifies the Location of the default attestation provider.</span></span>

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

### <span data-ttu-id="18a79-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="18a79-124">-Name</span></span>
<span data-ttu-id="18a79-125">Nazwa poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="18a79-125">Attestation Name.</span></span>

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

### <span data-ttu-id="18a79-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a79-126">-ResourceGroupName</span></span>
<span data-ttu-id="18a79-127">Określa nazwę grupy zasobów skojarzonej z zapytaniem o atestowanie.</span><span class="sxs-lookup"><span data-stu-id="18a79-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="18a79-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18a79-128">-ResourceId</span></span>
<span data-ttu-id="18a79-129">Określa nazwę pola Zasób skojarzonego z atestacją, do których jest ponawiane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="18a79-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="18a79-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a79-130">CommonParameters</span></span>
<span data-ttu-id="18a79-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a79-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a79-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18a79-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a79-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18a79-133">INPUTS</span></span>

### <span data-ttu-id="18a79-134">System.String</span><span class="sxs-lookup"><span data-stu-id="18a79-134">System.String</span></span>

## <span data-ttu-id="18a79-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18a79-135">OUTPUTS</span></span>

### <span data-ttu-id="18a79-136">Microsoft.Azure.Commands.Attestation.Models.PSAttastation</span><span class="sxs-lookup"><span data-stu-id="18a79-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="18a79-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="18a79-137">NOTES</span></span>

## <span data-ttu-id="18a79-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18a79-138">RELATED LINKS</span></span>
