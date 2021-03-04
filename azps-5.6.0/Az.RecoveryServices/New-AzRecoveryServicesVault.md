---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 811ac8b9f8922844dd5153a4fa02abc4c023f7a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953306"
---
# <span data-ttu-id="a7b13-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a7b13-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="a7b13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7b13-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b13-103">Tworzy nowy magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a7b13-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="a7b13-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a7b13-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7b13-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a7b13-105">DESCRIPTION</span></span>
<span data-ttu-id="a7b13-106">Polecenie **cmdlet New-AzRecoveryServicesVault** tworzy nowy magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a7b13-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="a7b13-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a7b13-107">EXAMPLES</span></span>

### <span data-ttu-id="a7b13-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a7b13-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="a7b13-109">Utwórz magazyn usługi odzyskiwania w grupie zasobów i w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a7b13-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="a7b13-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7b13-110">PARAMETERS</span></span>

### <span data-ttu-id="a7b13-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b13-111">-DefaultProfile</span></span>
<span data-ttu-id="a7b13-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b13-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7b13-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a7b13-113">-Location</span></span>
<span data-ttu-id="a7b13-114">Określa nazwę lokalizacji geograficznej magazynu.</span><span class="sxs-lookup"><span data-stu-id="a7b13-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="a7b13-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a7b13-115">-Name</span></span>
<span data-ttu-id="a7b13-116">Określa nazwę magazynu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="a7b13-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="a7b13-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7b13-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7b13-118">Określa nazwę grupy zasobów platformy Azure, w której chcesz utworzyć lub z której pobrać określony obiekt Usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a7b13-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="a7b13-119">— Tag</span><span class="sxs-lookup"><span data-stu-id="a7b13-119">-Tag</span></span>

<span data-ttu-id="a7b13-120">Określa tagi do dodania do magazynu usług odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="a7b13-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b13-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7b13-121">-Confirm</span></span>
<span data-ttu-id="a7b13-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a7b13-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7b13-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7b13-123">-WhatIf</span></span>
<span data-ttu-id="a7b13-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7b13-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7b13-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a7b13-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7b13-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b13-126">CommonParameters</span></span>
<span data-ttu-id="a7b13-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7b13-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b13-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7b13-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b13-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7b13-129">INPUTS</span></span>

### <span data-ttu-id="a7b13-130">Brak</span><span class="sxs-lookup"><span data-stu-id="a7b13-130">None</span></span>

## <span data-ttu-id="a7b13-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7b13-131">OUTPUTS</span></span>

### <span data-ttu-id="a7b13-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="a7b13-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a7b13-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a7b13-133">NOTES</span></span>

## <span data-ttu-id="a7b13-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7b13-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7b13-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a7b13-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="a7b13-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a7b13-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="a7b13-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a7b13-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


