---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: cdde8169c4b068b986910dc3bfc5de446833f5ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183819"
---
# <span data-ttu-id="a3877-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a3877-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="a3877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3877-102">SYNOPSIS</span></span>
<span data-ttu-id="a3877-103">Aktualizuje msi do magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a3877-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="a3877-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3877-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3877-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3877-105">DESCRIPTION</span></span>
<span data-ttu-id="a3877-106">To polecenie cmdlet służy do dodawania lub usuwania msi z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a3877-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="a3877-107">Użyj paramu -IdentityType, aby przypisać tożsamość systemową do RSVault.</span><span class="sxs-lookup"><span data-stu-id="a3877-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="a3877-108">Użyj identitytype none, aby usunąć msi z magazynu.</span><span class="sxs-lookup"><span data-stu-id="a3877-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="a3877-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3877-109">EXAMPLES</span></span>

### <span data-ttu-id="a3877-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3877-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="a3877-111">To polecenie cmdlet służy do dodawania tożsamości systemuAssigned do magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a3877-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="a3877-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3877-112">PARAMETERS</span></span>

### <span data-ttu-id="a3877-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3877-113">-DefaultProfile</span></span>
<span data-ttu-id="a3877-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3877-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3877-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a3877-115">-Name</span></span>

<span data-ttu-id="a3877-116">Określa nazwę magazynu usług odzyskiwania do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="a3877-116">Specifies the name of the recovery services vault to update.</span></span>

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

### <span data-ttu-id="a3877-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3877-117">-ResourceGroupName</span></span>

<span data-ttu-id="a3877-118">Określa nazwę grupy zasobów platformy Azure, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a3877-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

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

### <span data-ttu-id="a3877-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a3877-119">-IdentityType</span></span>
<span data-ttu-id="a3877-120">Typ MSI przypisany do magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a3877-120">The MSI type assigned to Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a3877-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3877-121">-Confirm</span></span>
<span data-ttu-id="a3877-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a3877-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3877-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3877-123">-WhatIf</span></span>
<span data-ttu-id="a3877-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3877-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3877-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a3877-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3877-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3877-126">CommonParameters</span></span>
<span data-ttu-id="a3877-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3877-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3877-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3877-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3877-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3877-129">INPUTS</span></span>

### <span data-ttu-id="a3877-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a3877-130">System.String</span></span>

## <span data-ttu-id="a3877-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3877-131">OUTPUTS</span></span>

### <span data-ttu-id="a3877-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span><span class="sxs-lookup"><span data-stu-id="a3877-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="a3877-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3877-133">NOTES</span></span>

## <span data-ttu-id="a3877-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3877-134">RELATED LINKS</span></span>
