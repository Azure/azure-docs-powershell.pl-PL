---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: cd6181ffb2bba8d71d8a0bf7cbe96d2f8038efc5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706850"
---
# <span data-ttu-id="63c9f-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="63c9f-101">Get-AzAttestation</span></span>

## <span data-ttu-id="63c9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="63c9f-103">Pobiera zaświadczenie.</span><span class="sxs-lookup"><span data-stu-id="63c9f-103">Gets an attestation.</span></span>

## <span data-ttu-id="63c9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63c9f-104">SYNTAX</span></span>

### <span data-ttu-id="63c9f-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="63c9f-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63c9f-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="63c9f-106">ResourceGroupParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63c9f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="63c9f-107">DESCRIPTION</span></span>
<span data-ttu-id="63c9f-108">Polecenie cmdlet Get-AzAttestation pobiera informacje o zaświadczeniu w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="63c9f-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="63c9f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63c9f-109">EXAMPLES</span></span>

### <span data-ttu-id="63c9f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="63c9f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```
<span data-ttu-id="63c9f-111">Pobierz zaświadczenie "przykład" w grupie zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="63c9f-111">Get Attestation "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="63c9f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63c9f-112">PARAMETERS</span></span>

### <span data-ttu-id="63c9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63c9f-113">-DefaultProfile</span></span>
<span data-ttu-id="63c9f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63c9f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63c9f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63c9f-115">-Name</span></span>
<span data-ttu-id="63c9f-116">Nazwa zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="63c9f-116">Attestation Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63c9f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63c9f-117">-ResourceGroupName</span></span>
<span data-ttu-id="63c9f-118">Określa nazwę grupy zasobów skojarzonej z poszukiwanym zaświadczeniem.</span><span class="sxs-lookup"><span data-stu-id="63c9f-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63c9f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63c9f-119">-ResourceId</span></span>
<span data-ttu-id="63c9f-120">Określa nazwę ResourceID skojarzonego z poszukiwanym zaświadczeniem</span><span class="sxs-lookup"><span data-stu-id="63c9f-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63c9f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63c9f-121">CommonParameters</span></span>
<span data-ttu-id="63c9f-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63c9f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63c9f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63c9f-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63c9f-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63c9f-124">INPUTS</span></span>

### <span data-ttu-id="63c9f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="63c9f-125">System.String</span></span>

## <span data-ttu-id="63c9f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63c9f-126">OUTPUTS</span></span>

### <span data-ttu-id="63c9f-127">Microsoft. Azure. Commands. zaświadczanie. modele. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="63c9f-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="63c9f-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63c9f-128">NOTES</span></span>

## <span data-ttu-id="63c9f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63c9f-129">RELATED LINKS</span></span>
