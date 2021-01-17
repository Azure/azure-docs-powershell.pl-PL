---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: cdde8169c4b068b986910dc3bfc5de446833f5ff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378287"
---
# <span data-ttu-id="8c6b3-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8c6b3-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="8c6b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6b3-103">Umożliwia zaktualizowanie Instalatora MSI do magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="8c6b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c6b3-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c6b3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8c6b3-105">DESCRIPTION</span></span>
<span data-ttu-id="8c6b3-106">To polecenie cmdlet umożliwia dodanie lub usunięcie MSI z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="8c6b3-107">Użyj parametru-IdentityType param, aby przypisać tożsamość SystemAssigned do RSVault.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="8c6b3-108">Nie usuwaj MSI z magazynu przy użyciu opcji IdentityType.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="8c6b3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c6b3-109">EXAMPLES</span></span>

### <span data-ttu-id="8c6b3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c6b3-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="8c6b3-111">To polecenie cmdlet umożliwia dodanie tożsamości SystemAssigned do magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="8c6b3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c6b3-112">PARAMETERS</span></span>

### <span data-ttu-id="8c6b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6b3-113">-DefaultProfile</span></span>
<span data-ttu-id="8c6b3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c6b3-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c6b3-115">-Name</span></span>

<span data-ttu-id="8c6b3-116">Określa nazwę magazynu usług Recovery Services do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-116">Specifies the name of the recovery services vault to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c6b3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c6b3-117">-ResourceGroupName</span></span>

<span data-ttu-id="8c6b3-118">Określa nazwę grupy zasobów platformy Azure, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c6b3-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8c6b3-119">-IdentityType</span></span>
<span data-ttu-id="8c6b3-120">Typ MSI przypisany do magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-120">The MSI type assigned to Recovery Services Vault.</span></span>

```yaml
Type: MSIdentity
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c6b3-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c6b3-121">-Confirm</span></span>
<span data-ttu-id="8c6b3-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c6b3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c6b3-123">-WhatIf</span></span>
<span data-ttu-id="8c6b3-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c6b3-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c6b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6b3-126">CommonParameters</span></span>
<span data-ttu-id="8c6b3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6b3-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c6b3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6b3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c6b3-129">INPUTS</span></span>

### <span data-ttu-id="8c6b3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8c6b3-130">System.String</span></span>

## <span data-ttu-id="8c6b3-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c6b3-131">OUTPUTS</span></span>

### <span data-ttu-id="8c6b3-132">Microsoft. Azure. Management. RecoveryServices. MODELES. magazyn</span><span class="sxs-lookup"><span data-stu-id="8c6b3-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="8c6b3-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c6b3-133">NOTES</span></span>

## <span data-ttu-id="8c6b3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c6b3-134">RELATED LINKS</span></span>
