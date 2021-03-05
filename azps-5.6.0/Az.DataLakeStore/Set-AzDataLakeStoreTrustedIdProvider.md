---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 7efe0e21b6b433160eab36856d3419dc918cbfc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995590"
---
# <span data-ttu-id="57f41-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="57f41-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="57f41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57f41-102">SYNOPSIS</span></span>
<span data-ttu-id="57f41-103">Modyfikuje określonego zaufanego dostawcę tożsamości w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="57f41-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="57f41-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="57f41-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57f41-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="57f41-105">DESCRIPTION</span></span>
<span data-ttu-id="57f41-106">Polecenie **cmdlet Set-AzDataLakeStoreTrustedIdProvider** modyfikuje określonego zaufanego dostawcę tożsamości w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="57f41-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="57f41-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="57f41-107">EXAMPLES</span></span>

### <span data-ttu-id="57f41-108">Przykład 1. Aktualizowanie punktu końcowego zaufanego dostawcy tożsamości</span><span class="sxs-lookup"><span data-stu-id="57f41-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="57f41-109">To aktualizuje punkt końcowy dostawcy dla reguły zapory "MyProvider" na koncie "ContosoADL" na https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="57f41-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="57f41-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57f41-110">PARAMETERS</span></span>

### <span data-ttu-id="57f41-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="57f41-111">-Account</span></span>
<span data-ttu-id="57f41-112">Konto usługi Data Lake Store w celu dodania zaufanego dostawcy tożsamości do usługi</span><span class="sxs-lookup"><span data-stu-id="57f41-112">The Data Lake Store account to add the trusted identity provider to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f41-113">-DefaultProfile</span></span>
<span data-ttu-id="57f41-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="57f41-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57f41-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="57f41-115">-Name</span></span>
<span data-ttu-id="57f41-116">Nazwa zaufanego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="57f41-116">The name of the trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f41-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="57f41-117">-ProviderEndpoint</span></span>
<span data-ttu-id="57f41-118">Prawidłowy punkt końcowy zaufanego dostawcy w formacie: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="57f41-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f41-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57f41-119">-ResourceGroupName</span></span>
<span data-ttu-id="57f41-120">Określa nazwę grupy zasobów zawierającej konto, dla których ma być aktualizowane zaufanego dostawcę tożsamości.</span><span class="sxs-lookup"><span data-stu-id="57f41-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="57f41-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57f41-121">-Confirm</span></span>
<span data-ttu-id="57f41-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="57f41-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57f41-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f41-123">-WhatIf</span></span>
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

### <span data-ttu-id="57f41-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f41-124">CommonParameters</span></span>
<span data-ttu-id="57f41-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f41-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f41-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57f41-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f41-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57f41-127">INPUTS</span></span>

### <span data-ttu-id="57f41-128">System.String</span><span class="sxs-lookup"><span data-stu-id="57f41-128">System.String</span></span>

## <span data-ttu-id="57f41-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57f41-129">OUTPUTS</span></span>

### <span data-ttu-id="57f41-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="57f41-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="57f41-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="57f41-131">NOTES</span></span>

## <span data-ttu-id="57f41-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57f41-132">RELATED LINKS</span></span>
