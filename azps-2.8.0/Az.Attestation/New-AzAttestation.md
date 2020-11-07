---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: ce21b116ceb41bfdfb26008dd44c914f3198ab39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706849"
---
# <span data-ttu-id="bbb13-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="bbb13-101">New-AzAttestation</span></span>

## <span data-ttu-id="bbb13-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbb13-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb13-103">Tworzy zaświadczenie</span><span class="sxs-lookup"><span data-stu-id="bbb13-103">Creates an attestation</span></span>

## <span data-ttu-id="bbb13-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbb13-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> [-AttestationPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbb13-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bbb13-105">DESCRIPTION</span></span>
<span data-ttu-id="bbb13-106">Polecenie cmdlet New-AzAttestation powoduje utworzenie zaświadczenia w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bbb13-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="bbb13-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbb13-107">EXAMPLES</span></span>

### <span data-ttu-id="bbb13-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bbb13-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```

<span data-ttu-id="bbb13-109">Tworzenie nowego zaświadczenia "przykład" w bieżącym Abonamentzie, Grupa zasobów "RG1"</span><span class="sxs-lookup"><span data-stu-id="bbb13-109">Create a new Attestation "example" in current Subscription, Resource Group "rg1"</span></span>

## <span data-ttu-id="bbb13-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbb13-110">PARAMETERS</span></span>

### <span data-ttu-id="bbb13-111">-AttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="bbb13-111">-AttestationPolicy</span></span>
<span data-ttu-id="bbb13-112">Określa przekazaną zasadę zaświadczania, w której ma zostać utworzone zaświadczenie.</span><span class="sxs-lookup"><span data-stu-id="bbb13-112">Specifies the attestation policy passed in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb13-113">-DefaultProfile</span></span>
<span data-ttu-id="bbb13-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbb13-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbb13-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bbb13-115">-Name</span></span>
<span data-ttu-id="bbb13-116">Określa nazwę tworzonego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="bbb13-116">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="bbb13-117">Nazwa może być dowolną kombinacją liter, cyfr lub łączników.</span><span class="sxs-lookup"><span data-stu-id="bbb13-117">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="bbb13-118">Nazwa musi zaczynać się i kończyć literą lub cyfrą.</span><span class="sxs-lookup"><span data-stu-id="bbb13-118">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="bbb13-119">Nazwa musi być uniwersalnie unikatowa.</span><span class="sxs-lookup"><span data-stu-id="bbb13-119">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb13-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbb13-120">-ResourceGroupName</span></span>
<span data-ttu-id="bbb13-121">Określa nazwę istniejącej grupy zasobów, w której ma zostać utworzone zaświadczenie.</span><span class="sxs-lookup"><span data-stu-id="bbb13-121">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb13-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbb13-122">-Confirm</span></span>
<span data-ttu-id="bbb13-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbb13-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb13-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbb13-124">-WhatIf</span></span>
<span data-ttu-id="bbb13-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbb13-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbb13-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bbb13-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb13-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb13-127">CommonParameters</span></span>
<span data-ttu-id="bbb13-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbb13-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb13-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbb13-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb13-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbb13-130">INPUTS</span></span>

### <span data-ttu-id="bbb13-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bbb13-131">System.String</span></span>

## <span data-ttu-id="bbb13-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbb13-132">OUTPUTS</span></span>

### <span data-ttu-id="bbb13-133">Microsoft. Azure. Commands. zaświadczanie. modele. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="bbb13-133">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="bbb13-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbb13-134">NOTES</span></span>

## <span data-ttu-id="bbb13-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbb13-135">RELATED LINKS</span></span>
