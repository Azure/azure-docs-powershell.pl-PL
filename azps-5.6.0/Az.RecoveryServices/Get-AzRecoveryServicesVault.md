---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: a6aa52408cf1befd1c1208258c184be327ff2a15
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971882"
---
# <span data-ttu-id="a9922-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a9922-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="a9922-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9922-102">SYNOPSIS</span></span>

<span data-ttu-id="a9922-103">Pobiera listę magazynów usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a9922-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="a9922-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a9922-104">SYNTAX</span></span>

### <span data-ttu-id="a9922-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9922-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9922-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9922-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9922-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a9922-107">DESCRIPTION</span></span>

<span data-ttu-id="a9922-108">Polecenie **cmdlet Get-AzRecoveryServicesVault** pobiera listę magazynów usług odzyskiwania w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a9922-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="a9922-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a9922-109">EXAMPLES</span></span>

### <span data-ttu-id="a9922-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9922-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="a9922-111">Pobierz listę magazynu w wybranej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a9922-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="a9922-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a9922-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="a9922-113">Pobierz listę magazynu w grupie zasobów w wybranej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a9922-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="a9922-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a9922-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="a9922-115">Pierwsze polecenie cmdlet pobiera magazyn w grupie zasobów o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="a9922-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="a9922-116">Następnie uzyskujemy dostęp do informacji MSI z magazynu.</span><span class="sxs-lookup"><span data-stu-id="a9922-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="a9922-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9922-117">PARAMETERS</span></span>

### <span data-ttu-id="a9922-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9922-118">-DefaultProfile</span></span>

<span data-ttu-id="a9922-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9922-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9922-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a9922-120">-Name</span></span>

<span data-ttu-id="a9922-121">Określa nazwę magazynu, dla których ma być kwerenda.</span><span class="sxs-lookup"><span data-stu-id="a9922-121">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9922-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9922-122">-ResourceGroupName</span></span>

<span data-ttu-id="a9922-123">Określa nazwę grupy zasobów platformy Azure, z której ma zostać pobrany określony obiekt Usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a9922-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9922-124">— Tag</span><span class="sxs-lookup"><span data-stu-id="a9922-124">-Tag</span></span>

<span data-ttu-id="a9922-125">Określa tagi, dla których ma być kwerenda</span><span class="sxs-lookup"><span data-stu-id="a9922-125">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9922-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="a9922-126">-TagName</span></span>

<span data-ttu-id="a9922-127">Określa klucz tagu do zapytania dla</span><span class="sxs-lookup"><span data-stu-id="a9922-127">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9922-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="a9922-128">-TagValue</span></span>

<span data-ttu-id="a9922-129">Określa wartość tagu dla zapytania</span><span class="sxs-lookup"><span data-stu-id="a9922-129">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9922-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9922-130">CommonParameters</span></span>
<span data-ttu-id="a9922-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9922-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9922-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9922-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9922-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9922-133">INPUTS</span></span>

### <span data-ttu-id="a9922-134">Brak</span><span class="sxs-lookup"><span data-stu-id="a9922-134">None</span></span>

## <span data-ttu-id="a9922-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9922-135">OUTPUTS</span></span>

### <span data-ttu-id="a9922-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="a9922-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a9922-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a9922-137">NOTES</span></span>
<span data-ttu-id="a9922-138">Get-AzRecoveryServicesVault w starej wersji usługi Az.RecoveryServices(<=2.10.0) nie może pracować z az.accounts(>=1.8.1) z powodu nieprawidłowego odwołania do zestawu.</span><span class="sxs-lookup"><span data-stu-id="a9922-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="a9922-139">Moduł Az.RecoveryServices wymaga uaktualnienia do wersji 2.11.0 lub nowszej, jeśli używasz najnowszej wersji az lub az.accounts.</span><span class="sxs-lookup"><span data-stu-id="a9922-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="a9922-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9922-140">RELATED LINKS</span></span>

[<span data-ttu-id="a9922-141">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a9922-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="a9922-142">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a9922-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="a9922-143">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a9922-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
