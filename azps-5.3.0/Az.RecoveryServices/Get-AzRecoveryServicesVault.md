---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: f667c0b13de510f7cf3e30e3faca9a93395ac221
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498545"
---
# <span data-ttu-id="9173a-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9173a-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="9173a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9173a-102">SYNOPSIS</span></span>

<span data-ttu-id="9173a-103">Pobiera listę magazynów usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="9173a-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="9173a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9173a-104">SYNTAX</span></span>

### <span data-ttu-id="9173a-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="9173a-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9173a-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9173a-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9173a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9173a-107">DESCRIPTION</span></span>

<span data-ttu-id="9173a-108">Polecenie cmdlet **Get-AzRecoveryServicesVault** pobiera listę magazynów usług odzyskiwania w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9173a-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="9173a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9173a-109">EXAMPLES</span></span>

### <span data-ttu-id="9173a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9173a-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="9173a-111">Pobierz listę magazynów w wybranej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9173a-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="9173a-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9173a-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="9173a-113">Pobierz listę magazynów w grupie zasób w wybranej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9173a-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="9173a-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9173a-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="9173a-115">Pierwsze polecenie cmdlet pobiera magazyn w grupie zasobów o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="9173a-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="9173a-116">Następnie uzyskujemy dostęp do informacji MSI z magazynu.</span><span class="sxs-lookup"><span data-stu-id="9173a-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="9173a-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9173a-117">PARAMETERS</span></span>

### <span data-ttu-id="9173a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9173a-118">-DefaultProfile</span></span>

<span data-ttu-id="9173a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9173a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9173a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9173a-120">-Name</span></span>

<span data-ttu-id="9173a-121">Określa nazwę magazynu, którego ma dotyczyć kwerenda.</span><span class="sxs-lookup"><span data-stu-id="9173a-121">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="9173a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9173a-122">-ResourceGroupName</span></span>

<span data-ttu-id="9173a-123">Określa nazwę grupy zasobów platformy Azure, z której ma zostać pobrany określony obiekt usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="9173a-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="9173a-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="9173a-124">-Tag</span></span>

<span data-ttu-id="9173a-125">Określa Tagi do zbadania</span><span class="sxs-lookup"><span data-stu-id="9173a-125">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="9173a-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="9173a-126">-TagName</span></span>

<span data-ttu-id="9173a-127">Określa klucz znacznika, dla którego ma zostać wyszukiwana kwerenda.</span><span class="sxs-lookup"><span data-stu-id="9173a-127">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="9173a-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="9173a-128">-TagValue</span></span>

<span data-ttu-id="9173a-129">Określa wartość tagu, dla którego ma zostać wyszukiwana kwerenda.</span><span class="sxs-lookup"><span data-stu-id="9173a-129">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="9173a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9173a-130">CommonParameters</span></span>
<span data-ttu-id="9173a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9173a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9173a-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9173a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9173a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9173a-133">INPUTS</span></span>

### <span data-ttu-id="9173a-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9173a-134">None</span></span>

## <span data-ttu-id="9173a-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9173a-135">OUTPUTS</span></span>

### <span data-ttu-id="9173a-136">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="9173a-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9173a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9173a-137">NOTES</span></span>
<span data-ttu-id="9173a-138">Get-AzRecoveryServicesVault w starej wersji AZ. RecoveryServices (<= 2.10.0) nie może działać z usługą AZ. accounts (>= 1.8.1) ze względu na niepoprawne odwołanie do zestawu.</span><span class="sxs-lookup"><span data-stu-id="9173a-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="9173a-139">Moduł AZ. RecoveryServices musi zostać uaktualniony do 2.11.0 lub nowszego, jeśli używasz najnowszych lub AZ. kont.</span><span class="sxs-lookup"><span data-stu-id="9173a-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="9173a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9173a-140">RELATED LINKS</span></span>

[<span data-ttu-id="9173a-141">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9173a-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="9173a-142">Nowe — AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9173a-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="9173a-143">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9173a-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
