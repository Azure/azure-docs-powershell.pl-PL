---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 6fa598b792d04d8223aafdb39405a69ada6e5915
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966641"
---
# <span data-ttu-id="fa06c-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="fa06c-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="fa06c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa06c-102">SYNOPSIS</span></span>
<span data-ttu-id="fa06c-103">Utwórz nowe wystąpienie szczegóły aplikacji Azure ActiveDirectory datamigration.</span><span class="sxs-lookup"><span data-stu-id="fa06c-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="fa06c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fa06c-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa06c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fa06c-105">DESCRIPTION</span></span>
<span data-ttu-id="fa06c-106">Utwórz nowe wystąpienie szczegóły aplikacji Azure ActiveDirectory datamigration.</span><span class="sxs-lookup"><span data-stu-id="fa06c-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="fa06c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fa06c-107">EXAMPLES</span></span>

### <span data-ttu-id="fa06c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fa06c-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="fa06c-109">ApplicationId: "Identyfikator AppId/Service Principal Id here" AppKey: System.Security.SecureString TenantId: "Identyfikator dzierżawy"</span><span class="sxs-lookup"><span data-stu-id="fa06c-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="fa06c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa06c-110">PARAMETERS</span></span>

### <span data-ttu-id="fa06c-111">- AppKey</span><span class="sxs-lookup"><span data-stu-id="fa06c-111">-AppKey</span></span>
<span data-ttu-id="fa06c-112">Klucz usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fa06c-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa06c-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fa06c-113">-ApplicationId</span></span>
<span data-ttu-id="fa06c-114">Identyfikator aplikacji usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fa06c-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa06c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa06c-115">-DefaultProfile</span></span>
<span data-ttu-id="fa06c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa06c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa06c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa06c-117">CommonParameters</span></span>
<span data-ttu-id="fa06c-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa06c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fa06c-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa06c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa06c-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa06c-120">INPUTS</span></span>

### <span data-ttu-id="fa06c-121">Brak</span><span class="sxs-lookup"><span data-stu-id="fa06c-121">None</span></span>

## <span data-ttu-id="fa06c-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa06c-122">OUTPUTS</span></span>

### <span data-ttu-id="fa06c-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="fa06c-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="fa06c-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fa06c-124">NOTES</span></span>

## <span data-ttu-id="fa06c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa06c-125">RELATED LINKS</span></span>
