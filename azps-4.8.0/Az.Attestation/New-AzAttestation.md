---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064562"
---
# <span data-ttu-id="3fea4-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="3fea4-101">New-AzAttestation</span></span>

## <span data-ttu-id="3fea4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fea4-102">SYNOPSIS</span></span>
<span data-ttu-id="3fea4-103">Tworzy zaświadczenie</span><span class="sxs-lookup"><span data-stu-id="3fea4-103">Creates an attestation</span></span>

## <span data-ttu-id="3fea4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fea4-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3fea4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3fea4-105">DESCRIPTION</span></span>
<span data-ttu-id="3fea4-106">Polecenie cmdlet New-AzAttestation powoduje utworzenie zaświadczenia w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3fea4-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="3fea4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fea4-107">EXAMPLES</span></span>

### <span data-ttu-id="3fea4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3fea4-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest4 -ResourceGroupName psh-test-rg -Location "East US" -Tags @{Test="true";CreationYear="2020"}                                                                                                                                                                                         
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest4
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest4
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest4.us.attest.azure.net
Tags              : {CreationYear, Test}
TagsTable         :
                    Name          Value
                    ============  =====
                    CreationYear  2020
                    Test          true
```

<span data-ttu-id="3fea4-109">Utwórz nowe wystąpienie dostawcy zaświadczania o nazwie *pshtest4* z kilkoma znacznikami i używając zaufania w usłudze AAD dla głównych zasad usługi tee.</span><span class="sxs-lookup"><span data-stu-id="3fea4-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="3fea4-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3fea4-110">Example 2</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg -Location "East US" -PolicySignersCertificateFile .\cert1.pem                                                                                                                                                
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest3
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest3
Status            : Ready
TrustModel        : Isolated
AttestUri         : https://pshtest3.us.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="3fea4-111">Utwórz nowe wystąpienie dostawcy zaświadczania o nazwie *pshtest3* ', który używa zaufania Isoladed dla głównych zasad tee za pośrednictwem określania zestawu zaufanych kluczy podpisywania za pośrednictwem pliku PEM.</span><span class="sxs-lookup"><span data-stu-id="3fea4-111">Create a new instance of an Attestation Provider named *pshtest3* \` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="3fea4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fea4-112">PARAMETERS</span></span>

### <span data-ttu-id="3fea4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fea4-113">-DefaultProfile</span></span>
<span data-ttu-id="3fea4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3fea4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fea4-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3fea4-115">-Location</span></span>
<span data-ttu-id="3fea4-116">Określa region platformy Azure, w którym ma zostać utworzony dostawca zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="3fea4-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="3fea4-117">Użyj polecenia Get-AzResourceProvider z parametrem ProviderNamespace, aby wyświetlić wybrane opcje.</span><span class="sxs-lookup"><span data-stu-id="3fea4-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fea4-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3fea4-118">-Name</span></span>
<span data-ttu-id="3fea4-119">Określa nazwę tworzonego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3fea4-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="3fea4-120">Nazwa może być dowolną kombinacją liter, cyfr lub łączników.</span><span class="sxs-lookup"><span data-stu-id="3fea4-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="3fea4-121">Nazwa musi zaczynać się i kończyć literą lub cyfrą.</span><span class="sxs-lookup"><span data-stu-id="3fea4-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="3fea4-122">Nazwa musi być uniwersalnie unikatowa.</span><span class="sxs-lookup"><span data-stu-id="3fea4-122">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fea4-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="3fea4-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="3fea4-124">Określa zestaw zaufanych kluczy podpisywania dla zasad wystawiania w jednym pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="3fea4-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fea4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fea4-125">-ResourceGroupName</span></span>
<span data-ttu-id="3fea4-126">Określa nazwę istniejącej grupy zasobów, w której ma zostać utworzone zaświadczenie.</span><span class="sxs-lookup"><span data-stu-id="3fea4-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fea4-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="3fea4-127">-Tag</span></span>
<span data-ttu-id="3fea4-128">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="3fea4-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fea4-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3fea4-129">-Confirm</span></span>
<span data-ttu-id="3fea4-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fea4-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fea4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fea4-131">-WhatIf</span></span>
<span data-ttu-id="3fea4-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fea4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fea4-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3fea4-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fea4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fea4-134">CommonParameters</span></span>
<span data-ttu-id="3fea4-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fea4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fea4-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fea4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fea4-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fea4-137">INPUTS</span></span>

### <span data-ttu-id="3fea4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3fea4-138">System.String</span></span>

### <span data-ttu-id="3fea4-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3fea4-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3fea4-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fea4-140">OUTPUTS</span></span>

### <span data-ttu-id="3fea4-141">Microsoft. Azure. Commands. zaświadczanie. modele. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="3fea4-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="3fea4-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fea4-142">NOTES</span></span>

## <span data-ttu-id="3fea4-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fea4-143">RELATED LINKS</span></span>
