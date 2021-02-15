---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203585"
---
# <span data-ttu-id="c8f46-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="c8f46-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="c8f46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8f46-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f46-103">Tworzy obiekt w celu zaktualizowania właściwości NIC serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="c8f46-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="c8f46-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c8f46-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8f46-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c8f46-105">DESCRIPTION</span></span>
<span data-ttu-id="c8f46-106">Polecenie New-AzMigrateNicMapping cmdlet tworzy mapowanie źródłowej karty NIC dołączonej do serwera do migrowania.</span><span class="sxs-lookup"><span data-stu-id="c8f46-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="c8f46-107">Ten obiekt jest dostarczany jako dane wejściowe do Set-AzMigrateServerReplication cmdlet w celu zaktualizowania nic i jego właściwości dla serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="c8f46-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="c8f46-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c8f46-108">EXAMPLES</span></span>

### <span data-ttu-id="c8f46-109">Przykład 1. Tworzenie obiektu NIC</span><span class="sxs-lookup"><span data-stu-id="c8f46-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="c8f46-110">Tworzy obiekt aktualizacji NIC.</span><span class="sxs-lookup"><span data-stu-id="c8f46-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="c8f46-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8f46-111">PARAMETERS</span></span>

### <span data-ttu-id="c8f46-112">- NicID</span><span class="sxs-lookup"><span data-stu-id="c8f46-112">-NicID</span></span>
<span data-ttu-id="c8f46-113">Określa identyfikator nic do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="c8f46-113">Specifies the ID of the NIC to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f46-114">- TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="c8f46-114">-TargetNicIP</span></span>
<span data-ttu-id="c8f46-115">Określa adres IP w docelowej podsieci, który ma być używany dla nic.</span><span class="sxs-lookup"><span data-stu-id="c8f46-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f46-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="c8f46-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="c8f46-117">Określa, czy nic nie będzie aktualizowany jako podstawowy, pomocniczy, czy nie.</span><span class="sxs-lookup"><span data-stu-id="c8f46-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f46-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="c8f46-118">-TargetNicSubnet</span></span>
<span data-ttu-id="c8f46-119">Określa nazwę podsieci dla nic w docelowej sieci wirtualnej, do której należy zmigrować serwer.</span><span class="sxs-lookup"><span data-stu-id="c8f46-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f46-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f46-120">CommonParameters</span></span>
<span data-ttu-id="c8f46-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f46-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f46-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8f46-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f46-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8f46-123">INPUTS</span></span>

## <span data-ttu-id="c8f46-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8f46-124">OUTPUTS</span></span>

### <span data-ttu-id="c8f46-125">Microsoft.Azure.PowerShell.Cmdlet.Migrate.Models.Api20180110.IVCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="c8f46-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="c8f46-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c8f46-126">NOTES</span></span>

<span data-ttu-id="c8f46-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c8f46-127">ALIASES</span></span>

## <span data-ttu-id="c8f46-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8f46-128">RELATED LINKS</span></span>

