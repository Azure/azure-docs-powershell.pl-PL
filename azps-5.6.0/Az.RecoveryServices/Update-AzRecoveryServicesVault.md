---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: 104bb05b4a01f5407c56e6c89de632a1ec5ab475
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970001"
---
# <span data-ttu-id="8bd70-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8bd70-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="8bd70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bd70-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd70-103">Aktualizuje msi do magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8bd70-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="8bd70-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8bd70-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bd70-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8bd70-105">DESCRIPTION</span></span>
<span data-ttu-id="8bd70-106">To polecenie cmdlet służy do dodawania lub usuwania msi z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8bd70-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="8bd70-107">Użyj param -IdentityType, aby przypisać tożsamość systemową przypisaną do RSVault.</span><span class="sxs-lookup"><span data-stu-id="8bd70-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="8bd70-108">Użyj identitytype none, aby usunąć msi z magazynu.</span><span class="sxs-lookup"><span data-stu-id="8bd70-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="8bd70-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8bd70-109">EXAMPLES</span></span>

### <span data-ttu-id="8bd70-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8bd70-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="8bd70-111">To polecenie cmdlet służy do dodawania tożsamości systemuAssigned do magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8bd70-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="8bd70-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bd70-112">PARAMETERS</span></span>

### <span data-ttu-id="8bd70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd70-113">-DefaultProfile</span></span>
<span data-ttu-id="8bd70-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd70-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bd70-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8bd70-115">-Name</span></span>

<span data-ttu-id="8bd70-116">Określa nazwę magazynu usług odzyskiwania do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="8bd70-116">Specifies the name of the recovery services vault to update.</span></span>

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

### <span data-ttu-id="8bd70-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bd70-117">-ResourceGroupName</span></span>

<span data-ttu-id="8bd70-118">Określa nazwę grupy zasobów platformy Azure, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8bd70-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

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

### <span data-ttu-id="8bd70-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8bd70-119">-IdentityType</span></span>
<span data-ttu-id="8bd70-120">Typ MSI przypisany do magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8bd70-120">The MSI type assigned to Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8bd70-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8bd70-121">-Confirm</span></span>
<span data-ttu-id="8bd70-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8bd70-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bd70-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bd70-123">-WhatIf</span></span>
<span data-ttu-id="8bd70-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bd70-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bd70-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8bd70-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bd70-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd70-126">CommonParameters</span></span>
<span data-ttu-id="8bd70-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd70-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd70-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bd70-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd70-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bd70-129">INPUTS</span></span>

### <span data-ttu-id="8bd70-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8bd70-130">System.String</span></span>

## <span data-ttu-id="8bd70-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bd70-131">OUTPUTS</span></span>

### <span data-ttu-id="8bd70-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span><span class="sxs-lookup"><span data-stu-id="8bd70-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="8bd70-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8bd70-133">NOTES</span></span>

## <span data-ttu-id="8bd70-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bd70-134">RELATED LINKS</span></span>
