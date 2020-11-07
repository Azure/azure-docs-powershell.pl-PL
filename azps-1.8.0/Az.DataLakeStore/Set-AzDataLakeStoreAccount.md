---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 0754bd515a846f8524bc7fd9826d36d19d79843a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868503"
---
# <span data-ttu-id="6137c-101">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6137c-101">Set-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="6137c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6137c-102">SYNOPSIS</span></span>
<span data-ttu-id="6137c-103">Modyfikuje konto w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6137c-103">Modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="6137c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6137c-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6137c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6137c-105">DESCRIPTION</span></span>
<span data-ttu-id="6137c-106">Polecenie cmdlet **Set-AzDataLakeStoreAccount** modyfikuje konto usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6137c-106">The **Set-AzDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="6137c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6137c-107">EXAMPLES</span></span>

### <span data-ttu-id="6137c-108">Przykład 1. Dodawanie znacznika do konta</span><span class="sxs-lookup"><span data-stu-id="6137c-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="6137c-109">To polecenie umożliwia dodanie określonego tagu do konta usługi Data Lake Store o nazwie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="6137c-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="6137c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6137c-110">PARAMETERS</span></span>

### <span data-ttu-id="6137c-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="6137c-111">-AllowAzureIpState</span></span>
<span data-ttu-id="6137c-112">Opcjonalnie Zezwalaj na używanie/blokowanie początkowych adresów IP platformy Azure za pośrednictwem zapory.</span><span class="sxs-lookup"><span data-stu-id="6137c-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6137c-113">-Domyślna</span><span class="sxs-lookup"><span data-stu-id="6137c-113">-DefaultGroup</span></span>
<span data-ttu-id="6137c-114">Określa identyfikator grupy katalogów usługi AzureActive.</span><span class="sxs-lookup"><span data-stu-id="6137c-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="6137c-115">Ta grupa jest domyślną grupą tworzonych plików i folderów.</span><span class="sxs-lookup"><span data-stu-id="6137c-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6137c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6137c-116">-DefaultProfile</span></span>
<span data-ttu-id="6137c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6137c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6137c-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="6137c-118">-FirewallState</span></span>
<span data-ttu-id="6137c-119">Opcjonalnie Włącz lub Wyłącz istniejące reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="6137c-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6137c-120">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="6137c-120">-KeyVersion</span></span>
<span data-ttu-id="6137c-121">Jeśli typ szyfrowania jest przypisany przez użytkownika, użytkownik może obrócić swoją wersję klucza za pomocą tego parametru.</span><span class="sxs-lookup"><span data-stu-id="6137c-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

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

### <span data-ttu-id="6137c-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6137c-122">-Name</span></span>
<span data-ttu-id="6137c-123">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6137c-123">Specifies the name of a Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6137c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6137c-124">-ResourceGroupName</span></span>
<span data-ttu-id="6137c-125">Określa nazwę grupy zasobów zawierającej konto usługi Data Lake Store do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="6137c-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6137c-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="6137c-126">-Tag</span></span>
<span data-ttu-id="6137c-127">Określa znaczniki jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="6137c-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="6137c-128">Za pomocą znaczników możesz identyfikować konta usługi Data Lake Store z innych zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6137c-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6137c-129">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="6137c-129">-Tier</span></span>
<span data-ttu-id="6137c-130">Pożądana warstwa zobowiązań do użycia dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="6137c-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6137c-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="6137c-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="6137c-132">Opcjonalnie Włącz lub Wyłącz istniejących dostawców zaufanych identyfikatorów.</span><span class="sxs-lookup"><span data-stu-id="6137c-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6137c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6137c-133">CommonParameters</span></span>
<span data-ttu-id="6137c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6137c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6137c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6137c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6137c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6137c-136">INPUTS</span></span>

### <span data-ttu-id="6137c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6137c-137">System.String</span></span>

### <span data-ttu-id="6137c-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6137c-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6137c-139">System. Nullable "1 [[Microsoft. Azure. Management. datalake. Store. MODELES. TrustedIdProviderState, Microsoft. Azure. Management. datalake. Store, wersja = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6137c-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6137c-140">System. Nullable "1 [[Microsoft. Azure. Management. datalake. Store. MODELES. FirewallState, Microsoft. Azure. Management. datalake. Store, wersja = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6137c-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6137c-141">System. Nullable "1 [[Microsoft. Azure. Management. datalake. Store......... usługi. Microsoft. Azure. Management. datalake. Store.</span><span class="sxs-lookup"><span data-stu-id="6137c-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6137c-142">System. Nullable "1 [[Microsoft. Azure. Management. datalake. Store. MODELES. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Store, wersja = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6137c-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="6137c-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6137c-143">OUTPUTS</span></span>

### <span data-ttu-id="6137c-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6137c-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="6137c-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6137c-145">NOTES</span></span>

## <span data-ttu-id="6137c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6137c-146">RELATED LINKS</span></span>

[<span data-ttu-id="6137c-147">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6137c-147">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6137c-148">Nowe — AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6137c-148">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6137c-149">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6137c-149">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6137c-150">Test — AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6137c-150">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


