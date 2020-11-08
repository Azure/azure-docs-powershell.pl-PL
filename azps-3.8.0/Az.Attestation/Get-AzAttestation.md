---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: a18222c40dc5c56bd2d67afb8d0df35b7aedc532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051706"
---
# <span data-ttu-id="c37b1-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="c37b1-101">Get-AzAttestation</span></span>

## <span data-ttu-id="c37b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c37b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c37b1-103">Pobiera zaświadczenie.</span><span class="sxs-lookup"><span data-stu-id="c37b1-103">Gets an attestation.</span></span>

## <span data-ttu-id="c37b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c37b1-104">SYNTAX</span></span>

### <span data-ttu-id="c37b1-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c37b1-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c37b1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c37b1-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c37b1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c37b1-107">DESCRIPTION</span></span>
<span data-ttu-id="c37b1-108">Polecenie cmdlet Get-AzAttestation pobiera informacje o zaświadczeniu w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="c37b1-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="c37b1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c37b1-109">EXAMPLES</span></span>

### <span data-ttu-id="c37b1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c37b1-110">Example 1</span></span>
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

<span data-ttu-id="c37b1-111">Pobierz *Pshtest* dostawcy zaświadczania w grupie zasób *PSH-test-RG*.</span><span class="sxs-lookup"><span data-stu-id="c37b1-111">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

## <span data-ttu-id="c37b1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c37b1-112">PARAMETERS</span></span>

### <span data-ttu-id="c37b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c37b1-113">-DefaultProfile</span></span>
<span data-ttu-id="c37b1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c37b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c37b1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c37b1-115">-Name</span></span>
<span data-ttu-id="c37b1-116">Nazwa zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="c37b1-116">Attestation Name.</span></span>

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

### <span data-ttu-id="c37b1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c37b1-117">-ResourceGroupName</span></span>
<span data-ttu-id="c37b1-118">Określa nazwę grupy zasobów skojarzonej z poszukiwanym zaświadczeniem.</span><span class="sxs-lookup"><span data-stu-id="c37b1-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="c37b1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c37b1-119">-ResourceId</span></span>
<span data-ttu-id="c37b1-120">Określa nazwę ResourceID skojarzonego z poszukiwanym zaświadczeniem</span><span class="sxs-lookup"><span data-stu-id="c37b1-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="c37b1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37b1-121">CommonParameters</span></span>
<span data-ttu-id="c37b1-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c37b1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37b1-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c37b1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37b1-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c37b1-124">INPUTS</span></span>

### <span data-ttu-id="c37b1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c37b1-125">System.String</span></span>

## <span data-ttu-id="c37b1-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c37b1-126">OUTPUTS</span></span>

### <span data-ttu-id="c37b1-127">Microsoft. Azure. Commands. zaświadczanie. modele. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="c37b1-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="c37b1-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c37b1-128">NOTES</span></span>

## <span data-ttu-id="c37b1-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c37b1-129">RELATED LINKS</span></span>
